<img src="https://render.fineartamerica.com/images/rendered/default/tote-bag/images/artworkimages/medium/2/eat-sleep-code-repeat-developer-life-sassy-lassy-transparent.png?&amp;targetx=64&amp;targety=0&amp;imagewidth=635&amp;imageheight=763&amp;modelwidth=763&amp;modelheight=763&amp;backgroundcolor=000000&amp;orientation=0&amp;producttype=totebag-18-18" alt="img" style="zoom:33%;" />

My mentor and I decided the **tasks** for this week given as :
* Study about the Tagged Context from the Concordances files for the concordance type experiemnt
* Extract Tagged context before, Tagged Query Item, Tagged Context after
* Extract Tag Caption, Before Time and after time of the file
* Display the left/right context according to display time on the Annotation Page

### Tagged Context (Aligned)
There are two types of tagged context relative to Tagged Query Item.
* Tagged Context Before. Example is as follows:

  ```python
  the_DT/265/68/265/79 group_NN/265/79/266/17 ._./265/NA/266/NA Came_VBD/267/10/267/16 back_RB/267/16/267/19 with_IN/267/54/267/79 a_DT/267/90/268/33 gallon_NN/268/77/269/25 of_IN/269/66/269/86 tide_NNP/270/36/270/62 laundry_NN/270/62/270/99 detergent_NN/270/99/271/49 and_CC/271/56/271/66 started_VBD/271/82/272/03 throwing_VBG/272/25/272/52 it_PRP/272/52/272/59 at_IN/272/59/272/61 people_NNS/272/90/273/36 ,_,/272/NA/273/NA UCW_NNP/276/17/276/50
  ```

  

* Tagged Context After. Example is as follows:

  ```python
  it_PRP/276/NA/277/NA at_IN/276/NA/277/NA them_PRP/278/74/278/77 ._./278/NA/279/NA Police_NN/280/17/280/50 in_IN/280/50/280/69 Portland_NNP/280/69/281/13 say_VBP/281/13/281/40 the_DT/281/40/281/63 size_NN/281/64/282/10 of_IN/282/10/282/20 the_DT/282/20/282/26 crowd_NN/282/26/282/60 may_MD/282/99/283/16 it_PRP/283/17/283/32 difficult_JJ/283/32/283/55 to_TO/283/77/283/90 respond_VB/283/90/284/34 to_TO/284/34/284/45 everything_NN/284/45/284/98
  ```

  

* Tagged Query Item

  ```python
  chucking_VBG/276/NA/277/NA
  ```

  
### Extraction of Caption, Before Time and After Time

I have written the following function to extract the Caption Text, Before Time and After. Also, while doing this I have taken care of unaligned text and some wrong unaligned text for example  ``3 1/<caption_text>/1034/5/1035/67`` using ``try and except`` functions.

```python
def getContextBTAT(string):
    txt = string.split("/")
    context = txt[0].split('_')[0]
    if txt[2] == 'NA':
        before_time = float(txt[1])
    else:
        try:
            before_time = float(txt[1]) + (float(txt[2])/100.0)
        except:
            before_time = float(txt[2])
    if txt[4] == 'NA':
        after_time = float(txt[3])
    else:
        try:
            after_time = float(txt[3]) + (float(txt[4])/100.0)
        except:
            after_time = float(txt[4])
    return context, before_time, after_time
```



### Getting Left/Right Context

I have used this function for getting the left/right context according to query time and before time and after time given by user in the ``DisplayTime`` dialog box.

```python
def getRequiredCaption(time_limit, context, operator):
    req_caption = ''
    for cpt in context:
        caption, bt, at = getContextBTAT(cpt)
        if operator(bt, time_limit):
            break
        req_caption = req_caption + caption + ' '
    return req_caption
```

 

### Displaying the Required Full Tagged Caption

I use this function for doing this.

```python
def get_tagged_context(inputPath, concordance_line_number, before_time, after_time):
    with open(inputPath, encoding='utf-8') as tsvfile:
            in_txt = csv.reader(tsvfile, delimiter = ',')
            text = list(in_txt)[concordance_line_number]
            tagged_context_before, tagged_quey_item, tagged_context_after = text[5], text[6], text[7]
            tagged_context_before = tagged_context_before.split(' ')
            tagged_context_before.reverse()
            tagged_context_after = tagged_context_after.split(' ')
    query_context, query_bt, query_at = getContextBTAT(tagged_quey_item)
    import operator as op
    left_caption = getRequiredCaption(query_bt - float(before_time), tagged_context_before, op.lt)
    right_caption = getRequiredCaption(query_bt + float(after_time), tagged_context_after, op.gt)
    left_caption = left_caption.split(' ')
    left_caption.reverse()
    req_tagged_caption = ' '.join(left_caption) + ' ' + query_context + ' ' + right_caption
    return req_tagged_caption
```

