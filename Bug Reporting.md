- Exploratory test session was completed on the 'Main' branch on 26/01/2023 in the morning, using Chrome.
- They were replicated on live link - https://gladimakers.netlify.app/#/dashboard using Firefox during write up
- Mac OS Ventura 13.1

Bugs are reported with a simple description, the steps to reproduce the bug and a rating based on the following:

* **1 - High:** Requires immediate attention
* **2 - Medium:** Should be addressed pre-deployment
* **3 - Low:** Can be addressed post-deployment

-------

### Description
screen resolution causing off centre and white bars due to different aspect ratio

Similarly, layout does re-arrange, but not optimised for mobile device


### Steps to reproduce
1. Load up gladimakers
2. expand the page to a size larger than Macbook Air
3. see sides and content

![[Screenshot 2023-01-26 at 10.53.19.png]]
![[Screenshot 2023-01-26 at 12.03.29.png]]
-  replicated on profile and start page

**OR**
1. load up and login to user (in this case Adam)
2. change display to a mobile size using dev tools
![[Screenshot 2023-01-26 at 13.11.43.png]]
### Defect management rating
**Low** - only visible on larger screens than the macbooks we are working from 
And - mobile devices may well be out of scope for this project

-----

### Description
The bubble backing to the 'Profile' button on the dashboard appears to have shrunk and is now not the same as the other buttons


### Steps to reproduce
1. Navigate to the Dashboard with any user
2. view profile button
![[Screenshot 2023-01-26 at 10.59.53.png]]


### Defect management rating
**Low** - just cosmetic at this point

---

### Description
Profile page doesn't display the experience level and equipment info correctly.

*This is only on first sign up and then navigating to the page a logout and login fixes this*


### Steps to reproduce
1. sign up with an account specifying the experience and equipment level
2. without logging out and logging back in - navigate to the profile page
3. see 'Info' section
![[Screenshot 2023-01-26 at 11.00.19.png]]


### Defect management rating
**Low** - only happens under a specific circumstance - and is still not vital

---

### Description
The set for maximal strength is inconsistent with the other two missing dash.

See the Maximal strength training 'sets'. The difference of the word 'to' and the '-'.


### Steps to reproduce
1. Navigate to the 'User Guide' page after logging in
2. See the info on the page
![[Screenshot 2023-01-26 at 11.03.16.png]]

### Defect management rating
**Low** - Minimal impact - just cosmetic at this point

-----

### Description
Logging out of a user, and then entering the URL for the dashboard does display the dashboard - with no data.

Would expect that this would either not display or maybe redirect to the login page or similar.

### Steps to reproduce
1. login to a valid user
2. log out of that user with one of the log out buttons
3. enter in the url 'http://localhost:8888/#/dashboard'
4. the below page displays
![[Screenshot 2023-01-26 at 11.07.40.png]]

### Defect management rating
**Medium** - allows for users to incorrectly use the site - but no data risk as data is blank

---

### Description
Pick an exercise popup could be confusing maybe should say pick a ‘category’ exercise.

For example, with 'Strength' selected, it would say 'Pick a strength exercise'

That way when viewing 'all' it would say:
Pick a Strength exercise
Pick a flexibility exercise
Pick a cardio exercise


### Steps to reproduce
1. Login and navigate to the Exercises Catalogue
2. Select one of the filters
![[Screenshot 2023-01-26 at 11.09.40.png]]


### Defect management rating
**Low** - Affects readability - but not functionality

---

### Description
#### NOTE - this bug was fixed at the time of showing the developers - on the live version of the product

Clicking on the exercise title throws a 'local host error' - maybe not connected to the description.

Would expect either the exercises to not be clickable - or have some predictable action upon clicking

### Steps to reproduce
1. Login and navigate to the Exercises Catalogue
2. click on any of the 'Exercises' next to the add to workout buttons
	1. eg - click 'curl'
![[Screenshot 2023-01-26 at 11.10.35.png]]

### Defect management rating
N/A

---

### Description
Muscles diagram on Exercises Catalogue page shows as clickable but does not provide an action

Would expect that clicking on either the text or the picture would show relevant exercises for this 

### Steps to reproduce
1. Login and navigate to the Exercises Catalogue
2. Scroll down and click on either the text or the diagram
![[Screenshot 2023-01-26 at 11.14.01.png]]

### Defect management rating
**Low** - Developers aware - still in development

-----

### Description
Timer does not reset when current exercise is 'removed'

would expect the timer to either reset, or maybe for it to stop the current workout

### Steps to reproduce
1. Login and go to the Exercise Catalogue
2. Add some exercises
3. return to the dashboard by clicking 'go to workout' (or otherwise)
4. start the workout and click remove on the active exercise
5. notice that the timer carries over to the next exercise and does not restart at 30
![[Screenshot 2023-01-26 at 11.22.11.png]]

![[Screenshot 2023-01-26 at 11.22.18.png]]

### Defect management rating
**Low** - does not break the workout 

------

### Description
Sometimes when modifying the selected exercises on the dashboard (by clicking remove) an exercise will get 'stuck'. This is often coupled with being unable to 'remove' one of the items and when clicking to remove the 'other item' it will remove all the items left.

Would expect to be able to remove any item whenever wanted
Would expect the timer not to get stuck repeating just one exercise rather than moving to the top.

Alternatively - maybe unable to remove items when the workout is active
or - if removing an item it stops the workout, and you can click to start from beginning

### Steps to reproduce
1. Login with a valid user and navigate to the 'exercise catalogue' page. 
2. Click All filter
3. Add 5 workouts
	1. Curl
	2. Squat
	3. bench press
	4. hamstring stretch
	5. front split
4. Click - go to workout!
5. click ' start workout. first up: curl'
6. wait for the timer to move onto squat (30 sec for exercise and then 10 for rest)
7. once the 'current exercise' is squat hover over the curl's remove button with your mouse and without moving the mouse click so you remove the items taht are there
	1. so remove curl, squat, bench press
8. notice that when you get to hamstring stretch, you cannot remove it
9. Allow the timer to elapse
10. notice that the current exercise will now be 'stuck' on Front Split
11. click the 'front split' remove button
12. notice that this removes both the remaining items
![[Screenshot 2023-01-26 at 11.26.15.png]]

Note - when demoing this with the developers on the 'live version' - this was displayed instead of the above issue. The content dissapears instead
![[Screenshot 2023-01-26 at 14.47.15.png]]
### Defect management rating
**Medium** - Does have an impact on functionality - but also, is quite specific to reproduce

---

### Description
Clicking the remove button on an exercise in the 'exercise catalogue', when there are multiple instances of that exercise, will remove all of that exercise.

Would expect that it only removes the 1 instance

### Steps to reproduce
1. Login and navigate to the exercise catalogue
2. add some exercises, making sure you add at least 2 of the same one (see skipping in the screens below)
3. click remove on one of them
4. notice that all skipping's have been removed
![[Screenshot 2023-01-26 at 11.12.19.png]]
![[Screenshot 2023-01-26 at 11.12.30.png]]

### Defect management rating

**Low** - does not break functionality - but does affect it

-----

### Description
Some of the headings are out of line with the buttons and appear close to them.

Would expect there to be space, and be in line
or to be on a separate line
### Steps to reproduce
1. Have logged in with the user 'Adam'
2. Navigate to the profile page
3. see formatting at the top of the page
![[image (4).png]]
### Defect management rating

**Low** - cosmetic at this point

----

### Description
Having 2 update buttons independently update the experience level and the equipment access was mildly confusing. No indication of update made

Would expect one update button a the bottom to update any modified details
Would expect a pop up or similar to make it clear the update has been made

### Steps to reproduce
1. log in with a valid user
2. navigate to the profile page
3. click on 'update details'
4. make a modification and notice both buttons are needed, and no indication of update is made 
	1. can navigate to the profile page of course and will see the changes made
![[Screenshot 2023-01-26 at 11.33.55.png]]
### Defect management rating
**Low** - Functionality still there, just could be clearer

----

### Description
History page within profile shows small '1s' on the calendar that when clicked display as 'events'. The account was made today so should probably not have an event listed on 25th (yesterday).

Would expect only days where workouts have been completed to have an indication of these

### Steps to reproduce
1. Created a new account
2. Navigate to the Profile page
3. Click on 'History'
4. notice the calendar has listings on 25th and 26th (as of today 27/01/2023)

This is even without completing a workout
![[Screenshot 2023-01-26 at 11.36.34.png]]
### Defect management rating
**Low** - seems to be in error - but not sure how much this is breaking intended functionality

----

### Description
Can sign up with what would expect to be an invalid user

Would expect the email field, and possibly the other fields as well, to throw an error if each have the entry '123'
Email is not a valid email
Maybe password is not complex enough (or similar)

### Steps to reproduce
![[Screenshot 2023-01-26 at 11.42.03.png]]

![[Screenshot 2023-01-26 at 11.42.15.png]]


### Defect management rating
**High** - the fields still check if there is duplication, but currently appears to be little/no validity checking

-----
