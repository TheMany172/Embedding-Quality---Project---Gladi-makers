# Gladiators Test Plan
​
## Overview
​
Gladiators is a website which allows you to create workout plans to meet your specific requirements and fitness goals.
As a user, I want to be able to create an account, sign in and view my dashboard. I want to be able to look at the list of exercises and track my daily exercise, as well as set goals for myself.
​
## Objective
​
This test plan intends to outline the testing which ensures the gladiators website carries out the below specified functional requirements. 
Add git workflow to the development branch for automated testing.
​
### Functional scope
​
We will only be testing the following functionality;
1. Sign up/ sign in
2. Exercise selection
3. Create workout plans, edit them
4. Check that random workout generator works
5. check that all workouts can be cleared 
6. check that workout can be marked complete 
7. check that date/time page works

​
## Test Environments
​
Tests will be performed using:
​
* Chromium engine 109
* Minimum network speed 20mbps
* Mac OS Ventura 13.1
* Automated testing performed with Playwright 1.28
* IntelliJ CE 2022.3.1
* JUnit 5.8.1
​
## Features To Be Tested
​
For each of the popular frameworks, we want to verify the following features:
​
1. Sign up
    - Can’t sign up with an empty username
	- Can’t sign up with an empty email address
	- Can’t sign up with an empty password
	- Can’t sign up with existing username
	- Can sign up with valid entries
		- New sign up form
			- buttons all work - redirect to dashboard
	- Home button
2. Sign in
    - Can’t sign in with an empty email
	- Can’t sign in with an empty password
	- Can sign in using keyboard
	- Can sign in using mouse
	- Can sign in using valid details
	- Home button
	- Sign up button
3. Gladiator Dashboard
	* Profile button displays profile (with correct name)
	* Spotify button
		* **No action**
	* Weather button
		* **No action**
	* Date/Time button
		* **No action**
	* Utilities button
		* Log out
			* if log out can still nav to dashboard (not loggedin - no data)
		* User Guide
			* displ
		* Facilities Finder
			* **No action**
		* Leaderboard
			* **No action**
		* Lifting Calculator
			* **No action**
		* Stop watch
			* **No action**
	- Exercise Catalogue button leads to relevant page
		- Yes
		- Go to workout button - does redirect to dashboard and shows selected workouts
			- highlights the current activity 
			- has rest
			- shows next
			- pausing works
			- 
	- Workout Complete
	- Clear All
		- Works fine
    - Do workout
        - timer and record each exercise finishing
    - Workout complete button
	    - **No action**
1. Exercise Catalogue
	- Dashboard
	- profile (pic)
	- logout
	- Filters work
		- ALL
		- Strength
		- Flexibility
		- Cardio
	- Clicking on all the exercises allow them to be added
	- Create/add exercises to workout plan
    - Click on muscle groups to show related exercises
2. Check that random workout generator works - May not work not added
    - Generate random workout
	    - **No action**
    - Click again to replace workout
- Profile Page
	- Displays info 
	- Update Details:
	- Milestones
		- blank page
	- History
		- incorrect data in calendar?

## Test Team
​
We have 3 testers available for this project in our test team.
The testers assigned to this project are:
* `A.Little` - Test Engineer who joined the company last week and is primarily 
still completing onboarding.
* `A.Patel` - Test Engineer who joined the company last week and is primarily 
still completing onboarding.
* `I.Pala` - Test Engineer who joined the company last week and is primarily 
still completing onboarding.
* `S.Rahman` - Test Engineer who joined the company last! week and is primarily 
still completing onboarding.
​
## Test Estimation/Schedule
Monday will be dedicated to setting up the test environments and some exploratory testing of the app in its current state.
The team is aware that the scheduled feature freeze is as of the end of Wednesday. As a result the best time for exploratory testing is after this, as without an accessible product, it cannot be explored other than by viewing the code still being written.
Adam is off on Monday - so some time will be spent on Tuesday assisting set up. Additionally, there is currently not a complete set of instructions so testers will make note of the needed steps to get someone up and running for the dev’s readme.
The remaining time on Tuesday and Wednesday will be aimed at implementing some CICD features.
Thursday will be committed to enacting testing on the product in it’s frozen state. Writing reports to show this work and informing the dev’s of anything found.

## Defect Management
​
When a tester encounters a bug, they will raise a defect on the GitHub Issues 
page for the project. The tester should assign one of the following priorities: 
​
* **1 - High:** Requires immediate attention
* **2 - Medium:** Should be addressed pre-deployment
* **3 - Low:** Can be addressed post-deployment
​
The list of defects will be reviewed on submission by the Development Team.
​
Product Owner will receive a daily update of outstanding and resolved number of defects.
​
​
## Entry Criteria
​
Testing will commence when:
​
* The testing team have been notified of the testing requirements and have access to the testing environment.
​
## Exit Criteria
​
The test plan has passed when all 3 frameworks have been tested according to the functional testing scope and any high and medium priority bugs have been addressed.
​
## Risks
​
The following table outlines all of the risks associated with this test plan, 
and how we intend to mitigate them:
​
| Risk | Mitigation | Priority |
| ---- | ---------- | -------- |
| Recent intermittent internet access in our office. | Allow testers to work from remote/home as needed. | Low |
| We might find more bugs than the developers have time to fix. | Follow the defect prioritisation and management policy | Medium |
| We've not tested to see how well the site performs with multiple users. | Arrange for some performance testing to happen after launch. | Medium |
| Compatability issues since entire testing env is using Mac and only testing Chrommium browsers | Schedule testing for other OS and browsers as more testers become available | Low |
| Time frame is very tight | Only testing for most important functionality to highlight major flaws | High |
​
## Test plan revision history
​
Here you will find a history of previous revisions of this test plan, with 
the name of the tester who authored the revision.
​
| Version | Author | Date |
| ------- | ------ | ---- |
| 1.0 (This version) | A.S.I.A | 16/01/2023 |
| 0.9 | T.Tester | 10/12/2022 |
| 0.8 | T.Tester | 10/10/2022 |

---------

