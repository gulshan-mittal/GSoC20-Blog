<img src="https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/GSOC.png?raw=true" alt="img" style="zoom:50%;" />

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

## Work Done for Evaluation 1

| S. No | Features Implemented | Status  |
|----|-----|-----|
| 1. |Fix: Multiple annotations occurring on the same item.|   ✅ |
| 2.|Fix: Limited length of captions|   ✅ |
| 3.| Made the annotation page more flexible |   ✅ |
| 4.|Users can download csv with full concordances along with target captions |   ✅ |
| 5.| Pagination of Annotation Results Page Enhanced|   ✅ |
| 6.|Added feature of optional displaying the target captions.|   ✅ |
| 7.|Delete All Files features in an experiment|   ✅ |
| 8.|Fix the Undo Functionality. (Need to be check again when display order becomes random)|   ✅ |

## A Walkthrough to the New Version of Rapid Annotator

* Feature to delete all the Files for an experiment.

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/1.png?raw=true)

* Display Caption are added on the Annotation Page so that user can just see to get some more context about the annotation process
    * Feature of displaying the target caption is optional.

    ![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/2.png?raw=true)

    * User can highlight the text by selecting a bunch of it and then it becomes the target caption.

    ![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/7.png?raw=true)

    * Target Caption will be saved when the annotation has been completed for a single file and for all the annotation levels of that particular file.
* Added Instruction field in the Annotaion Levels.

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/8.png?raw=true)

* The below image is showing the annotation instruction on the annotation page.

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/6.png?raw=true)

* You can direct navigate to the first and last page of the annotation results page.

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/3.png?raw=true)

* Feature of Downloading the whole Concordance

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/4.png?raw=true)


* Save results by annotator so that inter-annotator agreement can be calculated. 99999 as reserved word for “no answer yet”.

![img](https://github.com/gulshan-mittal/GSoC20-Blog/blob/master/assets/images/5.png?raw=true)
