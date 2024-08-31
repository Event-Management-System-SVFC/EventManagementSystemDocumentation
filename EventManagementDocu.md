# PlanIt: An Event Managemnt System

## A. Introduction

Event has many interpretations depending on how and what is your situation. It can be your birthday celebration, an important meeting, life changing events, your line of work, and many other events that you organize, or you attend. According to Saluja (2023), planning an event brings problems like last-minute changes, time management issues, technical difficulties, guest list management, registration issues, etc. Event management system or EMS is the solution for these problems.


A software program that assists in event planning, promotion, and execution is called an Event Management System (EMS). Its goal is to make event planning and administration easier by tracking event data, automating activities, and offering marketing and collaboration tools (Mohan, 2023). The system aims to provide centralized managing of details, important event related notifications, user management module, event management module, agenda management, create invitation links, guest listing, staff listing, and manage event status If it is cancelled, ended or currently ongoing. 


## B. Project Features and Characteristics
The proposed project Event management system consists of the following features:
1.	Event Management Module: This is where that main feature of the system will be found. Organizers can create events, delete events, organize event agendas, guest listing, staff listing, centralized event details manager, manage attendees, and organizer’s personal preferences.
2.	User Management Module: Organizers are required to create an account using verified email to make an event to save all the event logs and important details for future references.
3.	Create Invitation Links: Organizers can choose to send an invitation link to only be invited people or to send it publicly so people can register and list their names. Invited people can view event details permitted by the organizer.
4.	Create account
5.	Create and manage events
6.	Create Agendas
7.	Share event details through invitation links
8.	Event related notifications and reminders
9.	Assign seating arrangements
10.	Guest and Attendee listings
11.	Real-time event status sharing
12.	Utilizing google maps for navigation

![image](https://github.com/user-attachments/assets/f33afa17-af85-4874-9a39-ba37ff02e065)



## C. Project Scope

PlanIt an Event Management System is proposed to help organizers and guests efficiently manage and participate in events. The system will cover event details such as scheduling and invitations. It aims to support organizers by providing accurate data, simplifying event planning, and improving the overall attendee experience through digitalization. The EMS will be available to event organizers, staff, and guests to ensure smooth flow and coordination during events. The Event Management System will enable event organizers to create and manage multiple events, handle seating arrangements, and allocate resources efficiently.

## D. Work breakdown Structure
![image](https://github.com/user-attachments/assets/1d7e13db-c9ff-4ab2-93e5-08980cdb733b)



## E. Functional Requirements

### User Requirements


| No. | Users | System Features | Requirement |
|-----|-----|-----|-----|
| 1 | Organizer | A. User Management Module | 1. The system must allow organizers to create an account by entering: |
|  |  |  | a. google mail |
|  |  |  | b. firstname |
|  |  |  | c. surname |
|  |  |  | d. password |
|  |  | B. Event Management Module | 1. The system must allow organizers to create an event by entering |
|  |  |  | a. Event title |
|  |  |  | b. Event Description |
|  |  |  | c. Event additional information |
|  |  |  | d. Event address |
|  |  |  | e. Event image |
|  |  |  | f. Event time start |
|  |  |  | g. Event time end |
|  |  |  | 2. The system must allow organizers to create invitation by entering: |
|  |  |  | a. Invitee name |
|  |  |  | b. Invitee type |
|  |  |  | c. Seat number |
|  |  |  | 3. The system must allow organizers to list attendees by entering: |
|  |  |  | a. Invitation id |
|  |  |  | b. Time in |
|  |  |  | c. Time out |
|  |  |  | 4. The system must allow organizers to create agenda for the event by entering: |
|  |  |  | a. Agenda name |
|  |  |  | b. Agenda time start |
|  |  |  | c. Agenda time end |
|  |  | C. Invitation links | 1. The system must allow organizers to create invitation links for guests. |
| 2 | Guest | A. Invitation links | 1. The system must allow invitees or guests to view the event details using the invitation links provided by the organizer. |
	
### Use Case

![image](https://github.com/user-attachments/assets/0102e9b0-a5db-49c5-8e7d-0144d438add0)


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

### Table 4: ORGANIZER

| FIELD NAME | DESCRIPTION | DATA TYPE | LENGTH | SAMPLE |
| ------ | ------ | ------ | ------ | ------ |
| ORGANIZER_ID            | Unique identification of organizer     | String        | 255        | Wemnkqlme21            |
| ORGANIZER_GMAIL         | Gmail of the organizer                 | String        | 255        | juantamad@gmail.com    |
| ORGANIZER_PASSWORD      | Hashed password of the organizer       | String        | 255        | qweasdqweqwe           |
| ORGANIZER_FIRSTNAME     | Firstname of the organizer             | String        | 255        | Juan                   |
| ORGANIZER_SURNAME       | Surname of the organizer               | String        | 255        | Tamad                  |

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




References:

https://www.eventible.com/learning/event-planning-problems-and-solutions/


https://www.eventzilla.net/blog/event-resources/event-management-system-everything-you-need-to-know/

