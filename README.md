# Skill-Swap-App
A mobile app where university students log the skills they can teach, the skills they want to learn, and plan skill-exchange sessions with local reminders, all offline on their own phone.
Course: Mobile Application Development Assignment: Assignment 1: Plan, Design and Prototype University: Pak Austria Fachhochschule Institute of Applied Sciences and Technology

Skill Swap App is a mobile application that enables users to exchange knowledge and learn new skills through a peer-to-peer skill-sharing platform. Users can create profiles, post skills they can teach, specify skills they want to learn, and connect with others for mutually beneficial learning opportunities. The app provides a simple and collaborative environment for students, freelancers, and lifelong learners to grow their skills without the need for paid courses.

 Group Information (Group 14)

| Member Name     | Student ID    | GitHub Profile  | Project Role |                           
| Muhammad Fuzail | B24S0540CS030 | [@MuhammadFuzail288](https://github.com/MuhammadFuzail288) | Lead Developer & Git Admin 
| Rabia Rafaqat   | B24S0230CS002 | [@RabiaRafaqat](https://github.com/RabiaRafaqat)           | UI/UX & Style Guide Designer 
| Javeria Imran   | B24S0524CS003 | [@Javer1x](https://github.com/Javer1x)           | Database Architect & Requirements Lead 

Project Description

Many university students have skills they could share, such as design, programming or languages, but cannot afford paid courses, while other students want to learn exactly those skills.

Skill Swap App lets a student keep one organised, searchable record of the skills they can teach, the skills they want to learn and the peers they plan to swap with. Each entry can carry an optional session date and time, and the app sends a local reminder so planned learning sessions are not forgotten.

Value proposition: For university students who want to learn new skills without paying for courses, Skill Swap App is a mobile app that lets them log skills they can teach and want to learn, plan swap sessions and get reminders, all offline on their own phone.

Example: Ali teaches Photoshop and wants to learn Web Development; Sara teaches Web Development and wants to learn Photoshop. Each logs the swap with a session time and gets a reminder.

Scope note: All data is stored locally on the device and there is no login, so each phone holds its own skill board. The app does not match users across devices; cross-device matching and cloud sync are Could features only.


Planned Features
Must
ID	Feature	Built in
FR-01	Add a skill post (name, skill offered, skill wanted, category, description, optional session date and time)	A3
FR-02	View a list of all saved skill posts	A3
FR-03	Open a post to view its full details	A3
FR-04	Edit an existing skill post	A3
FR-05	Delete a skill post after confirming	A3
FR-06	Search skill posts by skill name	A3
FR-07	Filter skill posts by category (Design, Programming, Marketing, Language Learning)	A3
FR-09	Validate required fields (name, skill offered, skill wanted) before saving	A3
FR-10	Store all posts locally on the device using Hive	A3
FR-11	Send a local notification reminder at the session date and time set on a post	A3

Should
ID	Feature	Built in
FR-08	Sort posts by newest, oldest or alphabetical order	A4
FR-12	Show a clear empty-state message when there are no posts or no search results	A4

Could
ID	Feature
C-01	Cloud backend with sync and cross-device matching of users
C-02	User accounts and authentication

Non-functional requirements
ID	Requirement
NFR-01	The home screen loads in under 3 seconds on the test device or emulator
NFR-02	All saved data remains available offline and after the app is restarted
NFR-03	All touch targets are at least 48 x 48 dp
NFR-04	Text and background colours meet a contrast ratio of at least 4.5:1


Screens (6)
#	Screen	Purpose
S1	Home (start screen)	Recent skill posts, search bar, + button
S2	Skill List	All skill posts
S3	Add Skill	Form to create a post
S4	Edit Skill	Form to edit a post
S5	Skill Detail	Full information, edit and delete, session reminder
S6	Search & Filter	Search by skill name, filter by category, sort
Navigation: bottom tab bar (Home, Skills, Search) with stack navigation for Add, Detail and Edit.


Design
Screen flow diagram
Home	Skill    List	Add    Skill
Home	Skill -> List	Add -> Skill
Edit Skill	   Skill Detail	   Search & Filter
Edit Skill	-> Skill Detail	-> Search & Filter


Theme: light theme.
Colour	     |  Hex	    |      Use
Muted teal	   #3C6E71	   Primary: buttons, active tab, selected filters
Deep blue	    #284B63	   Secondary: app header, secondary actions, emphasis
White	        #FFFFFF	   Background: screens and cards
Charcoal	     #353535	   Text: headings, names, body text
Light gray	   #D9D9D9	   Borders, dividers, tag backgrounds
Font: Poppins. Icons: Material Icons (rounded). 
All text and background pairs meet a contrast ratio of at least 4.5:1.


Tech Stack
Component	              Choice
Framework	        Flutter (cross-platform)
Language	         Dart
Data storage	     Hive (local NoSQL database)
Notifications	    Flutter local-notifications package (final package confirmed in A3)
IDE	              Android Studio with Flutter and Dart plugins
Test target	       Android Emulator and/or physical Android phone
Version control	   Git and GitHub



Target platform: Android.
Data model (Hive box skill_posts)
Field	        |  Type     |	 Description
id	              Integer	  Unique key of the post
name	            Text    Name of the person in the exchange
offeredSkill    	Text	   Skill the person can teach
wantedSkill	     Text	   Skill the person wants to learn
description  	   Text	  Extra details
category	        Text	  Design, Programming, Marketing or Language Learning
createdDate	     DateTime	  When the post was created
sessionDateTime	 DateTime 
                (optional)	  planned session time; triggers the local                                 reminder


Setup Instructions
Prerequisites
Flutter SDK installed and added to your PATH
Android Studio with the Flutter and Dart plugins
An Android emulator (created in Android Studio) or a physical Android phone with USB debugging enabled
Git


Run the project
# 1. Clone the repository
git clone https://github.com/MuhammadFuzail288/Skill-Swap-App.git
cd Skill-Swap-App

# 2. Check that your environment is ready
flutter doctor

# 3. Install dependencies
flutter pub get

# 4. Start an emulator (or connect a phone), then run the app
flutter run


Project Structure
Skill-Swap-App/
├── docs/            # Report, wireframes and diagrams
├── lib/             # Flutter app source code
├── android/         # Android platform files
├── test/            # Tests
├── pubspec.yaml     # Dependencies
└── README.md

Planned layout inside lib/ (created in Assignment 2): main.dart, theme/, models/, data/, screens/, widgets/.



Project Roadmap
Assignment	Focus	Status
A1	Plan, design and prototype: idea, requirements, tech stack, screen flow, wireframes, style guide, project setup	In this repository
A2	User interface and navigation: all six screens with dummy data, style guide applied	Planned
A3	Data and functionality: Hive database, CRUD, validation, search, filter, local notifications	Planned
A4	Testing, polish and delivery: sort, empty states, tests, release APK, demo video, final documentation	Planned


Team Working Agreement
Communication: WhatsApp group for daily updates; Discord for calls when needed
Meetings: at least one team meeting per week, plus a short check before each deadline
Workflow: main always contains working code; each member works on a feature branch and merges through a pull request reviewed by another member
Merge conflicts: resolved together on a call before merging
Missed tasks: reported on WhatsApp at least 24 hours before the deadline; the group reassigns or shares the task
