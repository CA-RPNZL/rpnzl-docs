Developed by [Carmina](https://github.com/CarminaF), [Emily](https://github.com/e-mehegan), [Stephen](https://github.com/StevieG46) and [Helen](https://github.com/hotteok219) for Coder Academy T3A2 assignment.

# Links
http://rpnzl.studio/

### Deployed website

- Client: https://rpnzl.netlify.app/
- Server: https://ca-rpnzl-15265a6e99eb.herokuapp.com/

### GitHub repository

- Client: [rpnzl-client](https://github.com/CA-RPNZL/rpnzl-client)
- Server: [rpnzl-server](https://github.com/CA-RPNZL/rpnzl-server)
- Docs: [rpnzl-docs](https://github.com/CA-RPNZL/rpnzl-docs)

### Jump to:

- [Part A](#part-a)
- [Part B](#part-b)

# Part B

## Part B Table of contents

- [Libraries](#libraries)
- [Source control methodology](#source-control-methodology)
- [Project management methodology](#project-management-methodology)
- [Task delegation methodology](#task-delegation-methodology)
- [Testing](#testing)
    - [Formal testing](#formal-testing)
    - [Manual bfrontend testing: development and production](#manual-backend-testing-development-and-production)
    - [Manual backend testing: development and production](#manual-backend-testing-development-and-production)
- [Screenshots](#part-b-screenshots)


## Libraries

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

## Source control methodology

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

## Project management methodology

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

## Task delegation methodology

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

## Testing

### Manual backend testing: development and production

#### User

##### Log in (User: hairstylist, admin or client)
    - Development URL: http://localhost:3000/login
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/login
    - HTTP Method: POST
    - Expected output: JWT, userId, isAdmin, isHairstylist
    - Result: PASS

![Dev Login](./docs/BackendTesting/DEV%20LOGIN%20(User%20Hairstylist%20Admin%20Client).png)

![Prod Login](./docs/BackendTesting/PROD%20LOGIN%20(User%20Hairstylist%20Admin%20Client).png)

##### Sign up
    - Development URL: http://localhost:3000/users 
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/users
    - HTTP Method: POST
    - Expected output: User details
    - Result: PASS

![Dev signup](./docs/BackendTesting/DEV%20SIGNUP.png)

![Prod signup](./docs/BackendTesting/PROD%20SIGNUP.png)

##### Update personal details
    - Development URL: http://localhost:3000/users/id/:id
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/users/id/:id
    - HTTP Method: PATCH
    - Expected output: User’s updated details
    - Result: PASS

![Dev update personal details](./docs/BackendTesting/DEV%20UPDATE%20PERSONAL%20DETAILS.png)

![Prod update personal details](./docs/BackendTesting/PROD%20UPDATE%20PERSONAL%20DETAILS.png)

##### Update password
    - Development URL: http://localhost:3000/change-password/:id
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/change-password/:id
    - HTTP Method: PATCH
    - Expected output: “Successfully change password”, able to login
    - Result: PASS

![Dev update password](./docs/BackendTesting/DEV%20UPDATE%20PASSWORD.png)

![Prod update password](./docs/BackendTesting/PROD%20UPDATE%20PASSWORD.png)

##### Delete user
    - Development URL: http://localhost:3000/users/id/:id
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/users/id/:id
    - HTTP Method: DELETE
    - Expected output: “User account and future appointments deleted successfully.” + deleted users’ details
    - Result: PASS

![Dev delete user](./docs/BackendTesting/DEV%20DELETE%20USER.png)

![Prod delete user](./docs/BackendTesting/PROD%20DELETE%20USER.png)


##### All users (admin)
    - Development URL: http://localhost:3000/users
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/users
    - HTTP Method: GET
    - Expected output: 
    - Result: PASS

![Dev all users (Admin)](./docs/BackendTesting/DEV%20ALL%20USERS%20(Admin).png)

![Prod all users (Admin)](./docs/BackendTesting/PROD%20ALL%20USERS%20(Admin).png)

##### Get user (self)
    - Development URL: http://localhost:3000/users/id/:id
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/users/id/:id
    - HTTP Method: GET
    - Expected output: User’s details
    - Result: PASS

![Dev get user](./docs/BackendTesting/DEV%20GET%20USER%20(Self).png)

![Prod get user](./docs/BackendTesting/PROD%20GET%20USER%20(Self).png)

#### Services

##### All services
    - Development URL: http://localhost:3000/services
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/services
    - HTTP Method: GET
    - Expected output: All services
    - Result: PASS

![Dev all services](./docs/BackendTesting/DEV%20ALL%20SERVICES.png)

![Prod all services](./docs/BackendTesting/PROD%20ALL%20SERVICES.png)


#### Appointments

##### Get appointments for client
    - Development URL: http://localhost:3000/appointments/user/:userId?pastAppt=false
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments/user/:userId?pastAppt=false
    - HTTP Method: GET
    - Expected output: All future appointments for a client
    - Result: PASS

![Dev get appointments for client](./docs/BackendTesting/DEV%20GET%20APPOINTMENTS%20FOR%20CLIENT.png)
![Prod get appointments for client](./docs/BackendTesting/PROD%20GET%20APPOINTMENTS%20FOR%20CLIENT.png)

##### Get appointments for hairstylists

    - Development URL: http://localhost:3000/appointments/hairstylist/:userid?pastAppt=false
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments/hairstylist/:userid?pastAppt=false
    - HTTP Method: GET
    - Expected output: All future appointments where the user is the hairstylist
    - Result: PASS

![Dev get all appointments for hairstylist](./docs/BackendTesting/DEV%20GET%20ALL%20APPOINTMENTS%20FOR%20HAIRSTYLIST.png)

![Prod get appointment for hairstylist](./docs/BackendTesting/PROD%20GET%20ALL%20APPOINTMENTS%20FOR%20HAIRSTYLIST.png)

##### Get a single appointment

    - Development URL: http://localhost:3000/appointments/id/:apptId
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments/id/:apptId
    - HTTP Method: GET
    - Expected output: All details for one appointment
    - Result: PASS

![Dev get single appointment](./docs/BackendTesting/DEV%20GET%20SINGLE%20APPOINTMENT.png)

![Prod get single appointment](./docs/BackendTesting/PROD%20GET%20SINGLE%20APPOINTMENT.png)

##### Delete an appointment

    - Development URL: http://localhost:3000/appointments/id/:apptId
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments/id/:apptId
    - HTTP Method: DELETE
    - Expected output: Details of the deleted appointment
    - Result: PASS

![Dev delete appointment](./docs/BackendTesting/DEV%20DELETE%20APPOINTMENT.png)

![Prod delete appointment](./docs/BackendTesting/PROD%20DELETE%20APPOINTMENT.png)

##### Book an appointment

    - Development URL: http://localhost:3000/appointments
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments
    - HTTP Method: POST
    - Expected output: Details of the new appointment
    - Result: PASS

![Dev book appointment](./docs/BackendTesting/DEV%20BOOK%20APPOINTMENT.png)

![Prod book appointment](./docs/BackendTesting/PROD%20BOOK%20APPOINTMENT.png)


##### Update an appointment

    - Development URL: http://localhost:3000/appointments/id/:apptId
    - Production URL: https://ca-rpnzl-15265a6e99eb.herokuapp.com/appointments/id/:id
    - HTTP Method: PATCH
    - Expected output: Details of the updated appointment
    - Result: PASS

![Dev update appointment](./docs/BackendTesting/DEV%20UPDATE%20APPOINTMENT.png)

![Prod update appointment](./docs/BackendTesting/PROD%20UPDATE%20APPOINTMENT.png)

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

## <a id="part-b-screenshots"></a> Screenshots

### End of Part A Week 1 / end of Sprint 2 - 10 December 2023

### End of Part A Week 2 - 17 December 2023

### End of Part A Week 3 / end of Sprint 3 - 24 December 2023

*[^ Jump to Part B Table of contents](#part-b-table-of-contents)*

***

# Part A

## Part A Table of contents

- [R1 Description](#r1-description)
    - [Purpose](#purpose)
    - [Functionality / features](#functionality--features)
    - [Target audience](#target-audience)
    - [Tech stack](#tech-stack)
- [R2 Dataflow diagram](#r2-dataflow-diagram)
- [R3 Application architecture](#r3-application-architecture)
- [R4 User stories](#r4-user-stories)
    - [User personas and user stories](#user-personas-and-user-stories)
    - [Revision and refinement of user stories](#revision-and-refinement-of-user-stories)
- [R5 Wireframes](#r5-wireframes)
- [R6 Project management](#r6-project-management)
    - [Planning methodology](#planning-methodology)
    - [Screenshots](#part-a-screenshots)

## R1 Description

### Purpose

We are developing a full-stack web application tailored for the hair salon, RPNZL, which is transitioning into the online realm. Previously, RPNZL managed appointments using pen and paper. Customers were limited to in-person visits or phone calls to enquire about appointment times and availability.

The primary purpose of the app is to provide customers the ability to self-manage their appointments, as well as offering visibility to RPNZL’s salon manager and hairstylists. By moving the appointment system online, RPNZL hopes to increase their online presence, improve efficiency, reduce errors and provide customers with the convenience of 24/7 appointment scheduling.

### Functionality / features

The application features day and time slot options, along with diverse service selections. It guarantees a dynamic and personalised interaction for each user. Users can manage their appointments effortlessly, with the ability to easily cancel or reschedule their appointments.

To expand on user experience, the application will require customers and staff to register and log in. This is to ensure the privacy and safety of customer information through secure user authentication and authorisation. Staff such as the salon manager or hairstylists, have access to a staff only dashboard. Staff will also be able to manage their appointments.

The full-stack web application will create a user-friendly appointment scheduling process for customers at RPNZL but also provides hairstylists with a client management system. Features such as secure logins, intuitive booking, and easy appointment management, will provide an elevating salon experience for both clients and staff.

Pricing may vary due to thickness and length of hair, therefore payments will be made at the salon after the appointment.

#### Appointment management

Users can:
- choose their preferred service and hairstylist,
- view a hairstylist’s availability,
- select a suitable day and time slot,
- make an appointment,
- view appointments,
- reschedule an appointment, and
- cancel an appointment.

#### Account management

Users can:
- register for a customer account,
- log in and log out of their account,
- view appointment details that’s only relevant to the user
- customers can only see their appointments
- hairstylists can see appointments that have been booked with them
- update their account details, and
- update their password.

#### Administrator functions
Additionally, the salon manager (administrator) can:
- create new salon services
- update existing salon services,
- remove salon services,
- register hairstylists for a staff account, and
- view, create, update and delete any/all appointments.

#### General pages
Users can find information about:
- the salon, reviews and images,
- the hairstylists,
- the services available, and
- the salon’s contact details.

### Target audience

RPNZL’s application is designed to cater to the needs of the customers, hairstylists and the salon manager. 

For existing and prospective customers, the application provides a convenient, online hair appointment system. The application is hassle-free, secure and provides a range of services with relevant information.

For the hairstylists and salon manager, the application aims to streamline their daily appointments. They will benefit from personal logins which grant them access to a dedicated dashboard for efficient appointment management.

### Tech stack

#### Front end

- [React](https://react.dev/)
- [Bootstrap](https://getbootstrap.com/)

#### Back end

- [Express](https://expressjs.com/)
- [Node.js](https://nodejs.org/en)

#### Database

- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)

#### Testing

- [Jest](https://jestjs.io/)

#### Deployment and hosting

- [Netlify](https://www.netlify.com/)
- [Heroku](https://www.heroku.com/)
- [MongoDB Atlas](https://www.mongodb.com/atlas/database)

#### Source control

- [GitHub](https://github.com/)

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

## R2 Dataflow diagram

Please open image in a new tab for better clarity.

![Dataflow Diagram](./docs/RPNZL_T3A2_DataflowDiagram.png)

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

## R3 Application architecture

Please open image in a new tab for better clarity.

![Application architecture diagram](./docs/RPNZL_T3A2_ApplicationArchitecture.jpg)

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

## R4 User stories

### User personas and user stories

#### First time customer

![First time customer](./docs/RPNZ_T3A2_UserStories_first-time-customer.png)

#### Regular customer

![Regular customer](./docs/RPNZ_T3A2_UserStories_regular-customer.png)

#### Hairstylist

![Hairstylist](./docs/RPNZ_T3A2_UserStories_hairstylist.png)

#### Salon manager

![Salon manager](./docs/RPNZ_T3A2_UserStories_salon-manager.png)

### Revision and refinement of user stories

- Originally the user persona referenced one type of customer. After initial research, we introduced 2 types of customers: a regular customer and a first-time customer. The first time customer might like services and features such as:
    - a hair consultation
    - photos of the hairstylist’s previous works.

  Therefore we introduced 2 new features to our system.
- Initially, the hairstylists could sign up for their own account. However, we realised there is nothing stopping the average person from making an account. Therefore, we changed it so only the salon manager can make a hairstylist's account.

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

## R5 Wireframes

[Figma Link](https://www.figma.com/file/bYxlYHjWs7hUZ7zzUOx1P3/RPNZL?type=design&node-id=1%3A13&mode=design&t=BYAt8CUQpq7hQ34U-1)

### Process
- We initiated the design process by creating low-fidelity wireframes to visualize potential layouts for the website pages. Following the conceptualization phase, we had a meeting to collaboratively evaluate and select the most promising wireframe ideas for each page, arriving on the final layout.

  We progressed to the creation of coloured wireframes. Multiple colour palette options were generated, and as a team, we discussed the preferred colour scheme and font for the site. The selected choices were then applied to develop the coloured wireframes, which were further detailed through annotations on a separate page.

### Desktop

![Desktop SS 1](./docs/desktop_full1.png)
![Desktop SS 2](./docs/desktop_full2.png)

### Tablet

![Tablet SS 1](./docs/tablet_full1.png)
![Tablet SS 2](./docs/tablet_full2.png)

### Mobile

![Mobile SS](./docs/mobile_full.png)

### Further screenshots of wireframes
Below are further screenshots of the wireframes including annotated wireframes that provide more detail.
<details>
  <summary>Low Fidelity: Wireframe Ideas</summary>
  
### Home
#### Desktop
![LF Desktop Home/Home Nav](./docs/LF_ideas/LF_DesktopHome.png)
#### Mobile/Tablet
![LF MobTab Home](./docs/LF_ideas/LF_MobTabHome.png)

### Login
#### Desktop
![LF Desktop Login](./docs/LF_ideas/LF_LoginDesktop.png)
#### Mobile/Tablet
![LF MobTab Login](./docs/LF_ideas/LF_MobTabLogin.png)

### Sign Up
#### Desktop
![LF Desktop Sign Up](./docs/LF_ideas/LF_SignUpDesktop.png)
#### Mobile/Tablet
![LF MobTab Sign Up](./docs/LF_ideas/LF_MobTabSignUp.png)

### Services
#### Desktop
![LF Desktop Services](./docs/LF_ideas/LF_ServicesDesktop.png)
#### Mobile/Tablet
![LF MobTab Services](./docs/LF_ideas/LF_MobTabServices.png)

### Contact Us
#### Desktop
![LF Desktop Contact Us](./docs/LF_ideas/LF_ContactDesktop.png)
#### Mobile/Tablet
![LF MobTab Contact Us](./docs/LF_ideas/LF_MobTabContact.png)

### About
#### Desktop
![LF Desktop About](./docs/LF_ideas/LF_AboutDesktop.png)
#### Mobile/Tablet
![LF MobTab About](./docs/LF_ideas/LF_MobTabAbout.png)

### Customer Portal
#### Desktop
![LF Desktop Customer Portal](./docs/LF_ideas/LF_CustPortDesktop.png)
#### Mobile/Tablet
![LF MobTab Customer Portal](./docs/LF_ideas/LF_MobTabCustPort.png)

### Staff Portal
#### Desktop
![LF Desktop Staff Portal](./docs/LF_ideas/LF_StaffPortDesktop.png)
#### Mobile/Tablet
![LF MobTab Customer Portal](./docs/LF_ideas/LF_MobTabStaffPort.png)

### Admin Portals
#### Desktop
![LF Desktop Admin](./docs/LF_ideas/LF_AdminPortDesktop.png)
#### Mobile/Tablet
![LF MobTab Admin](./docs/LF_ideas/LF_MobAdminPort.png)

### Booking Process Pages
#### Desktop
![LF Desktop Booking](./docs/LF_ideas/LF_DesktopBooking.png)
#### Mobile/Tablet
![LF MobTab Booking](./docs/LF_ideas/LF_MobTabBooking.png)
</details>

<br />

<details>
  <summary>Final: Low Fidelity</summary>

#### Desktop
![Final Desktop 1](./docs/FLF/FLF_Desktop1.png)
![Final Desktop 2](./docs/FLF/FLF_Desktop2.png)
![Final Desktop 3](./docs/FLF/FLF_Desktop3.png)
![Final Desktop 4](./docs/FLF/FLF_Desktop4.png)
![Final Desktop 5](./docs/FLF/FLF_Desktop5.png)

#### Tablet
![Final Tablet 1](./docs/FLF/FLF_Tablet1.png)
![Final Tablet 2](./docs/FLF/FLF_Tablet2.png)
![Final Tablet 3](./docs/FLF/FLF_Tablet3.png)
![Final Tablet 4](./docs/FLF/FLF_Tablet4.png)

#### Mobile
![Final Mobile 1](./docs/FLF/FLF_Mobile1.png)
![Final Mobile 2](./docs/FLF/FLF_Mobile2.png)
![Final Mobile 3](./docs/FLF/FLF_Mobile3.png)
![Final Mobile 4](./docs/FLF/FLF_Mobile4.png)
</details>

<br>

<details>
  <summary>Coloured Wireframes: Annotated</summary>

### Home
#### Desktop
![Desktop Home](./docs/desktop_home.png)
![Desktop Home Nav](./docs/desktop_homeNav.png)
#### Mobile/Tablet
![MobTab Home](./docs/mobTab_Home.png)

### Login
#### Desktop
![Desktop Login](./docs/desktop_login.png)
#### Mobile/Tablet
![MobTab Login](./docs/mobTab_login.png)

### Sign Up
#### Desktop
![Desktop Sign Up](./docs/desktop_signup.png)
#### Mobile/Tablet
![MobTab Sign Up](./docs/mobTab_signUp.png)

### Services
#### Desktop
![Desktop Services](./docs/desktop_services.png)
#### Mobile/Tablet
![MobTab Services](./docs/mobTab_services.png)

### Contact Us
#### Desktop
![Desktop Contact Us](./docs/desktop_contactUs.png)
#### Mobile/Tablet
![MobTab Contact Us](./docs/mobTab_contactUs.png)

### About
#### Desktop
![Desktop About](./docs/desktop_about1.png)
![Desktop About 2](./docs/desktop_about2.png)
#### Mobile/Tablet
![MobTab About](./docs/mobTab_about.png)

### Customer Portal
#### Desktop
![Desktop Customer Portal](./docs/desktop_custport.png)
#### Mobile/Tablet
![MobTab Customer Portal](./docs/mobTab_customerport.png)

### Staff Portal
#### Desktop
![Desktop Staff Portal](./docs/desktop_staffport.png)
#### Mobile/Tablet
![MobTab Staff Portal](./docs/mobTab_staffport.png)

### Admin Portals
#### Desktop
![Desktop Admin 1&2](./docs/desktop_admin12.png)
![Desktop Admin 3&4](./docs/desktop_admin34.png)
![Desktop Admin 5](./docs/desktop_admin5.png)
#### Mobile/Tablet
![MobTab Admin 1&2](./docs/mobTab_admin12.png)
![MobTab Admin 3&4](./docs/mobTab_admin34.png)
![MobTab Admin 5](./docs/mobTab_admin5.png)

### Booking Process Pages
#### Desktop
![Desktop Booking 1&2](./docs/desktop_booking12.png)
![Desktop Booking 3](./docs/desktop_booking3.png)
![Desktop Booking 4](./docs/desktop_booking4.png)
![Desktop Booking 5](./docs/desktop_booking5.png)
#### Mobile/Tablet
![MobTab Booking 1&2&3](./docs/mobTab_booking123.png)
![MobTab Booking 4&5](./docs/mobTab_booking45.png)

</details>

<br />

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

## R6 Project management

### Planning methodology

For our project management board, we used Trello.

Trello board: [https://trello.com/b/Jz9YZmmt/rpnzl](https://trello.com/b/Jz9YZmmt/rpnzl)

### Sprints and stand ups

We set up our sprints to be two week blocks, with a sprint planning meeting at the start of the sprint.

- **Sprint 1** - Sunday 12 November - Saturday 25 November
    - Sprint planning meeting: Sunday 12 November @ 7:00pm ACDT / 7:30pm AEDT
- **Sprint 2** - Sunday 26 November - Saturday 9 December
    - Sprint planning meeting: Sunday 26 November @ 7:00pm ACDT / 7:30pm AEDT
- **Sprint 3** - Sunday 10 December - Sunday 23 December
    - Sprint planning meeting: Sunday 10 December @ 7:00pm ACDT / 7:30pm AEDT

For Sprint 1, we decided to have daily stand ups at 6:30pm ACDT / 7pm AEDT, Monday to Friday.

Saturdays and Sundays were open for optional, ad hoc meetings instead.

For each stand up, notes were taken to accommodate any absences for the day, which allowed team members to catch up.

For Sprint 2 and 3, we would reflect on Sprint 1 before making any decisions.

### Trello board guidelines

#### Column definitions

Our Trello board is divided into 5 columns:
- **Resources**
    - For easy access to the card template, Trello guidelines, Git guidelines and Sprint & stand ups.
- **To Do**
    - Cards sit here until they’re allocated a sprint.
    - Cards can, but do not need to be assigned to a team member in this column.
    - Cards can, but do not need a due date.
- **In Progress**
    - Cards move here when they’re in the current sprint and actively being worked on.
    - All cards in this column should have at least one assignee.
    - All cards in this column should have at least one sprint label.
    - All cards in this column should have a due date.
- **Review / Test**
    - Cards move here when they’re being reviewed or tested.
    - All cards in this column should have at least one assignee.
    - All cards in this column should have at least one sprint label.
    - All cards in this column should have a due date.
- **Done**
    - Cards move here when they’re completed (100%).
    - All cards in this column should have at least one assignee (members who actioned and members who reviewed).
    - All cards in this column should have at least one sprint label.
    - All cards in this column should have a due date.

#### Other guidelines

- Using the card template, select **Create card from template** to create a new card.
- Every card should have an assignee (unless it’s in **To do** / **Resources**).
- Every card should have a due date (unless it’s in **To do** / **Resources**).
- Every card should have a label indicating difficulty (**Simple** / **Challenging** / **Complex**).
- During sprint planning:
    - cards in **To do** should be allocated to a team member.
    - cards should be given the appropriate sprint label (**Sprint 1** / **Sprint 2** / **Sprint 3**).
    - cards should be moved to **In progress** when they're being worked on.
- If a card is not completed by the end of sprint, the card should be labelled with both the original and next sprint (e.g. a task was complex so it was labelled with **Sprint 2** and **Sprint 3**).
- In the card description, enter a summary of the task (if applicable).
- In the card description, enter the name of the primary lead on the feature and the reviewer.
- Use checklists feature.
- Comments:
    - Use comments to tag someone specific if you want to ask a question / ask for advice etc.
    - Use comments to track updates, adaptations or changes that are made.
    - Post related Git commit links when you merge to main.
    - Post other related links such as Diagram.io or Figma links.

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*

### <a id="part-a-screenshots"></a> Screenshots

#### Start of Sprint 1 - 13 November 2023

![Screenshot of Trello board - Part A - start](./docs/screenshot-trello-parta-1-start.jpg)

#### Middle 1 of Sprint 1 - 17 November 2023

##### Screenshot 1 of 2

![Screenshot of Trello board - Part A - middle 1 (1 of 2)](./docs/screenshot-trello-parta-2-mid1A.png)

##### Screenshot 2 of 2 (‘Done’ column scrolled all the way down)

![Screenshot of Trello board - Part A - middle 1 (2 of 2)](./docs/screenshot-trello-parta-3-mid1B.png)

#### Middle 2 of Sprint 1 - 22 November 2023

![Screenshot of Trello board - Part A - middle 2](./docs/screenshot-trello-parta-4-mid2.png)

#### End of Part A - 29 November 2023

##### Screenshot 1 of 2
![Screenshot of Trello board - Part A - end (1 of 2)](./docs/trelloSS_end1.png)

##### Screenshot 2 of 2
![Screenshot of Trello board - Part A - end (2 of 2)](./docs/trelloSS_end2.png)

*[^ Jump to Part A Table of contents](#part-a-table-of-contents)*