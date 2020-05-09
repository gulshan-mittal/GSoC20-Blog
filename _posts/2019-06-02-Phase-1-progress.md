---
layout: post
title: "Phase 1 Progress"
---

It is a great feeling to work on the Red Hen Rapid Annotator-2.0 Project and adding production level code in the project. This post includes all my work which will be done during the Phase 1 evaluation. This phase is directly headed towards the coding part of the project.

# [](#header-1)Decisions made post community bonding period

After the community bonding period several changes has been redefined and there has been addition of two taks. The following things is decided on several deliberation with the mentors:
1. There should a admin CRUD in the project. Admins should be able to see and access all experiments.
2. It would be perfect to have an "export to Rapid Annotator" button in CQPweb. -&gt; Waiting for the feedback from Andrew Hardie to implement this feature.
3. Add support for tagging Scheme is redefined. Now in the tagging scheme the annotation labels can be reused by the user for other experiments as well. This will save user's time a lot and provide a more comprehensible way for the annotations.

# [](#header-2) Work Done for Evaluation 1

| S. No | Features Implemented | Status  |
|---|-----|-----|
| 1. |Enhancements According to User Feedback Report includes (Community Bondind Period Work)|   ✅ |
| 2.|Addition of Admin in the experiment. Now, Admins should be able to see and access all others experiments.|   ✅ |
| 3.| Resolve issue of the green warning over the login and sign up buttons |   ✅ |
| 4.|Added “Undo” functionality for the last element in the set of annotations.|   ✅ |
| 5.|Include Video link and captions in the result export.|   ✅ |
| 6.|Added support for tagging Scheme|   ✅ |
| 7.|Added functionality of pausing the video with the space and again play it using the space key|   ✅ |
| 8.|Displaying a warning, If labels are changed when the annotators have started the annotation process.|   ✅ |
| 9.|Add support for randomizing the display order| In progress|
| 10.|Add support for partitioning the data for multiple annotators| In discussion with mentors|



# [](#header-3) Progress made so far

The following features has been implemented till so far:

* Addition of Admin in the experiment. Now, Admins should be able to see and access all others experiments.

![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/Admin.png?raw=true)

* When starting not logged in at an address of frontapge, the green warning is over the login and sign up buttons, so these are not accessible. Now these buttons are made accessible and the green warning now automatically fades out after some time.

![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/war1.png?raw=true)

* Added "Undo" functionality for the last element in the set of annotations.
    * One Done button is added, if clicked then the annotations can't undergoes undo process. If undo button is clicked then annotation goes to previous level including last annotation as well. Given below image is showing undo on last annotation.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/undo1.png?raw=true)

    * Restoring of previous Annotation for annotating again.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/undo2.png?raw=true)

* Include Video link and captions in the result export.

![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/excel1.png?raw=true)

* Added support for tagging Scheme. Now in the tagging scheme the annotation labels can be reused by the user for other experiments as well. This will save user's time a lot and provide a more comprehensible way for the annotations. Below Images are showing the tagging scheme
    * One Global Button is added if clicked then the annotation levels of that experiment can be re-used by the user (others users also). The status of Global button is changes to Private to remove the annotations level from the import list. User can import annotation levels by clicking on **Import Existing Levels**.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag1.png?raw=true)

    * Selecting the desired levels user want.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag2.png?raw=true)


    * If Annotation levels imported successfully then the feedback appears to him.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag3.png?raw=true)

    * If Annotation levels are already imported, then the feedback appears to him that you have already imported the levels.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag4.png?raw=true)

    * Now, user is able to see the annotation levels on the label page.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag5.png?raw=true)

* Added functionality of pausing the video with the space and again play it using the space key.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/pause.gif?raw=true)

* Displaying a warning, If labels are changed when the annotators have started the annotation process.

    * In the following image one more label "spring" is added to the existing labels.

        ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/changed_lables.png?raw=true)
    
    * Now, the warning is shown to the annotators when they try to annotate the data.

        ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/warning_labels.png?raw=true)

