![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/GSOC.png?raw=true)

Working during Community Period is Awesome and is a great experience to me. This post includes my work which I have done during Phase 1 Period. I utilized the community bonding period to discuss the deliverables with my mentors **Peter Uhrig**, **Anna Wilson**, and **Vaibhav Gupta**.


## Meeting Gist

Here is a summary of points that we would like to address this summer. This is not necessarily complete - we are still exploring.

* Fix: Anna encountered limitations on the number of levels and labels at 5 to 8 levels, which should not be there. We will investigate this on cluos.
* Fix: Multiple annotations occurring on the same item.
* Fix: Limited length of captions
* Make the annotation page more flexible:
    * Add instruction field to each level so students can read up on what they need to do.
    * Allow for a free text field (again, configurable) in addition to the other labels
    * Add a method to edit the captions by the annotator; not only text but possibly Rich Text, e.g. allowing for highlighting etc. -> make this configurable (is it allowed or not); keep original caption and include both in the download. Have a functional annotation for the target, e.g. <target>aslkfjasdlkjf</target> and make that a separate column in the database and download.
* Download/upload:
    * allow for CSV; [PROBLEM: Germans and other strange people with odd CSV formats; we will probably ignore this.]
    * consider using pandas for both Excel import/export and for CSV import/export
    * Store entire CQPweb concordance and include all fields in download plus the annotations and captions (both original and changed - see above)
* Allow for different context definitions with aligned data: n words to the left or right; this sentence; n sentences left/right; this sentence + 5 seconds before; etc. and display only the corresponding words in the caption.
* Change database:
    * Save results by annotator so that inter-annotator agreement can be calculated. 99999 as reserved word for “no answer yet”.
* Save results by annotator so that inter-annotator agreement can be calculated. 99999 as reserved word for “no answer yet”.
    * By randomizer
    * By clustering algorithm (Himani’s GSoC project)
* If time: CQPweb integration, although I get the feeling our users are quite happy to be able to work with the concordances before uploading them to the Rapid Annotator, so this may not be such an important feature after all.

## Installing version of RapidAnnotator on Gallo Account

We are also installing a testing version of rapidannotator at Gallo account on Red Hen's Server. We have installed it partially as we are getting some errors in library versions nad MariaDB version.

We will adress this also during this phase.