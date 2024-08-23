## A. Introduction

## B. Project Features and Characteristics
The proposed project Event management system consists of the following features:
1. Event credentials including the staff, attendees or the participants of the events.The use of event credentials can identify who are the attendees by using of badges, wristbands or any materials.
2.  Agenda scheduling for locations, event planning, update schedule and customization.
3.  User module for users credential.
4.  VRM for arrangement of bookings.

## C. Project Scope

The Event Management System (EMS) is proposed to help organizers and user efficiently manage and participate in events. The system will cover event details such as scheduling, venue booking, attendee registration, and payment processing. It aims to support organizers by providing accurate data, simplifying event planning, and improving the overall attendee experience through digitalization. The EMS will be available to event organizers, staff, and user to ensure smooth communication and coordination during events.

The Event Management System will enable event organizers to create and manage multiple events, book venues, handle seating arrangements, and allocate resources efficiently. Attendees will be able to register for events, view personalized schedules, and make online payments. However, the EMS will focus on facilitating in-person events and will not support hosting virtual events at this stage. Additionally, the system will not offer features for large-scale virtual conferencing or event streaming.

## D. Work breakdown Structure
![image](https://github.com/user-attachments/assets/7d0ef25f-4a52-4091-af3f-eb1c3a973633)


## E. Functional Requirements

### User Requirements

| No. | Users      | System Features                                          | Requirement                                                                                                                                                |
|-----|------------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Organizer  | A. User Module - User Details                 | 2. The system must allow the Organizer to view user details:                                                                                                          |
|     |            |                                                          |    a. User Name                                                                                                                                            |
|     |            |                                                          |    b. User Email                                                                                                                                           |
|     |            |                                                          |    c. Record of the Schedule                                                                                                                               |
|     |            |                                                          |    d. Record of the Event Credentials                                                                                                                      |
| 2   | Users      | A. User Module - Register                     | 1. The system must allow the users to log in to the web by entering:                                                                                                  |
|     |            |                                                          |    a. First Name                                                                                                                                           |
|     |            |                                                          |    b. Last Name                                                                                                                                            |
|     |            |                                                          |    c. Email address                                                                                                                                        |
|     |            |                                                          |    d. Password                                                                                                                                             |
|     |            |                                                          |    e. Confirm Password                                                                                                                                     |
|     |            | B. User Module - Login                        | 2. The system must allow the users to log in to the web by entering:                                                                                                  |
|     |            |                                                          |    a. Email address                                                                                                                                        |
|     |            |                                                          |    b. Password                                                                                                                                             |
|     |            | C. Agenda Scheduling                                     | 3. The system must allow the users to create their personalized schedule by entering:                                                                      |
|     |            |                                                          |    a. Event Title                                                                                                                                          |
|     |            |                                                          |    b. Location                                                                                                                                             |
|     |            |                                                          |    c. Time Start                                                                                                                                           |
|     |            |                                                          |    d. Time End                                                                                                                                             |
|     |            |                                                          |    e. Event Menu (Optional)                                                                                                                                |
|     |            |                                                          |    f. Event Description                                                                                                                                    |
|     |            |                                                          |    g. Event Image                                                                                                                                          |
|     |            | D. Event Credentials                        | 4. The system must allow the users to enter the name of:                                                                                                                |
|     |            |                                                          |    a. Event Planner                                                                                                                                        |
|     |            |                                                          |    b. Event Staff                                                                                                                                          |
|     |            |                                                          |    c. Event Attendees                                                                                                                                      |


### Use Case

![USE CASE](https://github.com/user-attachments/assets/c98428c4-a6bc-4fab-9f78-8c69eafd2b28)


## F. Database Architecture

### Data Dictionary

### Table 1: EVENT

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| EVENT_ID                          | Unique Identification of event                                     | String        | 255        | eqwiasdWqs123                                      |
| EVENT_TITLE                       | Title of the event                                                 | String        | 255        | Wedding                                            |
| EVENT_DESCRIPTION                 | Description of the event                                           | String        | 255        | The wedding of Joy and Mark                        |
| EVENT_ADDITIONAL_INFORMATION      | Additional information specific for the event                      | String        | 255        | Dress code, Food Menu, Etc.                        |
| EVENT_ADDRESS                     | Address where the event will be held (plain text or Google Maps link) | String        | 255        | Example City, Sampaguita St., or https://www.google.com/maps |
| EVENT_PLANNER                     | ID of the user who planned this event                              | String        | 255        | Eqlkeqwlk123                                       |
| EVENT_IMAGE                       | Link of the image of the event                                     | String        | 255        | https://firebase.com/image.png                     |
| IS_EVENT_CANCELLED                | If the event is cancelled by the user                              | Boolean       |            | false                                              |
| IS_EVENT_ENDED                    | If the event is already ended                                      | Boolean       |            | true                                               |
| IS_EVENT_ONGOING                  | If the event is currently happening                                | Boolean       |            | false                                              |
| EVENT_TIME_START                  | Datestamp when the event will start                                | Date          |            | 09-24-2002, 12:20                                  |
| EVENT_TIME_END                    | Datestamp when the event will end                                  | Date          |            | 09-25-2002, 12:20                                  |

### Table 2: ATTENDEES

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| ATTENDEE_ID     | Unique identification of attendee                      | String        | 255        | Qwinesq12             |
| INVITATION_ID   | Unique identification of invitation                    | String        | 255        | Qwiwwenesq12          |
| TIME_IN         | Date and time of the arrival of the attendee at the venue | Date          |            | 09-24-2002, 12:20      |
| TIME_OUT        | Date and time of the exit of the attendee at the venue    | Date          |            | 09-24-2002, 12:20      |

### Table 3: INVITED

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| INVITATION_ID     | Unique identification of invitation         | String        | 255        | Qweopqwe23q         |
| INVITED_NAME      | Name of the invited person                  | String        | 255        | Juan Tamad          |
| EVENT_ID          | Unique identification of event              | String        | 255        | Qweopwwqwe23q       |
| ATTENDEE_TYPE     | Type or Role of the attendee                | String        | 255        | Host, Singer, DJ    |
| SEAT_NUMBER       | Seat number of the invited person in the event | Int           | 55         | 1                   |

### Table 4: USER

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| USER_ID            | Unique identification of user     | String        | 255        | Wemnkqlme21            |
| USER_GMAIL         | Gmail of the user                 | String        | 255        | juantamad@gmail.com    |
| USER_PASSWORD      | Hashed password of the user       | String        | 255        | qweasdqweqwe           |
| USER_FIRSTNAME     | Firstname of the user             | String        | 255        | Juan                   |
| USER_SURNAME       | Surname of the user               | String        | 255        | Tamad                  |

### Table 5: AGENDA

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| AGENDA_ID            | Unique identification of the agenda               | String        | 255        | Webqjwke120         |
| EVENT_ID             | Unique identification of the event                | String        | 255        | 11Webqjwke120       |
| AGENDA_NAME          | Name of the agenda                                | String        | 255        | Lunch               |
| AGENDA_TIME_START    | Starting Date and Time stamp of the agenda        | Date          |            | 09-24-2002, 13:30   |
| AGENDA_TIME_END      | Ending Date and Time stamp of the agenda          | Date          |            | 09-24-2002, 14:30   |

### ERD

![EMS drawio (1)](https://github.com/user-attachments/assets/d86e354d-00f3-4cf4-8a39-f169b6b812db)

