---
layout: post
title: "Phase 2 Progress"
---

It is a great feeling to work on the Red Hen Rapid Annotator-2.0 Project and adding production level code in the project. This post includes all my work which will be done during the Phase 2 evaluation. This phase is directly headed towards the coding part of the project.

# [](#header-1)Decisions made post Phase 1

After the phase 1 evaluation some features has been redefined. The following things is decided on several deliberation with the mentors:
1. There will be a warning on edit, delete and add label data modal on the Label Page. This will enable user to understand if any changes made by him/her can effect the annotations in progress.
2. Add support for tagging Scheme is redefined.  Now there will be a Global Name for all the Annotation levels belonging to an experiment. User can import all annotation levels belonging to that Global Name. 

# [](#header-2) Work Done for Evaluation 2

| S. No | Features Implemented | Status  |
|---|-----|-----|
| 1. |Implemented changes suggested in Tagging Scheme|   ✅ |
| 2.|Displaying a warning, If labels are changed when the annotators have started the annotation process. On the Label Page also.|   ✅ |
| 3.| Implemented Progress Bar and Progress Status on the Annotation page. | ✅ |
| 4. | Implemented Account Menu in nav-bar which contain Settings for Updating Information, check Progress and logout sections. | ✅ |
| 5. | Implemented functionality to Update the Profile Information | ✅ |
| 6. | Implemented functionality to check the progress of other annotators assigned be a user and also provide a way to check the progress of a user which is included in the experiment. | ✅ |
| 7. | Corrected the Bug of Displaying Names when a user is added as a Owner or as an annotator. | ✅ |
| 8. | Now the Display time can take Float values with the precision of .01 seconds. | ✅ |
| 9. | Space Bar Cannot be used as a Key for the Annotations as it is used for pausing/playing the videos. | ✅ |
| 10. | Registration Process is Authenticated by validating the user's email. | ✅ |
| 11. | Forgot Password functionality is added. Now a user has to verify his email by entering an OTP sent to his email. | ✅ |

# [](#header-3) Progress made so far

The following features has been implemented in Phase 2 till so far:

* **Added support for tagging Scheme**. Now in the tagging scheme the annotation labels can be reused by the user for other experiments as well. This will save user's time a lot and provide a more comprehensible way for the annotations. Now when user click on Make global button (Description; A button for making the experiment global so that other users can import it) then a dialog box will open in which a user can put the name (global name) for all the annotation levels that a user will while importing that annotations. I have implemented the scheme in which a user can import all the annotation levels of a particular experiment. I have done this because as a User it feels so easy to just import all the annotation levels and delete one or two according to his/her comfort. If we have done this in another way like importing single annotation level then it becomes so cumbersome to import 10 annotation levels of a single experiment and later if he needs only say 8 so the user has to do same efforts as he/she would do in other method. Below Images are showing the tagging scheme
  

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag11.png?raw=true)


    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag6.png?raw=true)
    
    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag7.png?raw=true)
    
    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag8.png?raw=true)


    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag9.png?raw=true)
    
    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/tag10.png?raw=true)


​    

​    

​    

* Displaying a warning, If labels are changed when the annotators have started the annotation process.

    * In the following image one more label "spring" is added to the existing labels.

        ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/changed_lables.png?raw=true)

    * Now, the warning is shown to the annotators when they try to annotate the data.

        ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/warning_labels.png?raw=true)

    * Now, the Label Warnings are also added on the Label Page.

        * When the User wants to edit the label

            ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/labels2.png?raw=true)

        * When the User wants to delete the label

            ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/label1.png?raw=true)

        * When the User wants to add more labels

            ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/labels3.png?raw=true)

        * When the User wants to delete annotation Levels.

            ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/labels4.png?raw=true)

* Progress bar and Progress Status is implemented on the Annotation Page. Now the user can track his/her performance. Progress Bar is looking Awesome! 

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/progress_bar.png?raw=true)

* Implemented Account Menu in nav-bar which contain Settings for Updating Information, check Progress and logout sections.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/account_info.png?raw=true)

* Implemented functionality to Update the Profile Information.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/update_info1.png?raw=true)

* Implemented functionality to check the progress of other annotators assigned be a user and also provide a way to check the progress of a user which is included in the experiment. Now a user can select the experiment from a drop-down list and can see the progress of that experiment by all the annotators in a bar chart type graph.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/check_progress.png?raw=true)

* Corrected the Bug of Displaying Names when a user is added as a Owner or as an annotator.  Earlier Full name is displayed which is a major fault as Full name can be same for two users.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/add_annotator.png?raw=true)

* Now the Display time can take Float values with the precision of .01 seconds means now the before and after time gap can be up to 0.01 seconds. 

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/display_time.png?raw=true)

* Space Bar Cannot be used as a Key for the Annotations as it is used for pausing/playing the videos.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/space_key.png?raw=true)

* Registration Process is Authenticated by validating the user's email. Now an email will be sent to the user for validating the email. The user has to click on the verification link to verify his account and then only the user can login to his/her account.

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/otp_1.png?raw=true)

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/otp_2.png?raw=true)

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/otp_3.png?raw=true)

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/otp_4.png?raw=true)

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/otp_5.png?raw=true) 

* Forgot Password functionality is added. Now a user has to verify his email by entering an OTP sent to his email. First the user has to enter his/her username and email address and then after an OTP is sent to the registered email. User has to enter that OTP for updating his/her password. 

    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/forgot_1.png?raw=true)


    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/forgot_2.png?raw=true)


    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/forgot_3.png?raw=true)


    ![image](https://github.com/gulshan-mittal/GSoC19-Blog/blob/master/assets/images/forgot_5.png?raw=true)


​    
​    

* All the above things have implemented with the necessary feedback, warnings and error logs. 