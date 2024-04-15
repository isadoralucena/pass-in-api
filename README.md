# Pass-in API

An application developed in Java using the Spring framework to manage participants in in-person events. This tool allows organizers to register events and open public registration pages, while participants can register for events, view their registration badges, and check-in on the day of the event.

## Endpoints

### Events

Method | Endpoint | Description
-------- | ---- | -----
POST | http://localhost:8080/events | Create an event
GET | http://localhost:8080/events/{eventId} | Get an event

### Attendees

Method | Endpoint | Description
-------- | ---- | -----
GET | http://localhost:8080/events/{eventId}/attendees | Get event attendees
POST | http://localhost:8080/events/{eventId}/register | Register and attendee
GET | http://localhost:8080/attendees/{attendeeId}/badge | Get an attendee badge

### Check-ins

Method | Endpoint | Description
-------- | ---- | -----
POST | http://localhost:8080/attendees/{attendeeId}/check-in | Check-in attendee

## Requirements

### Functional Requirements

- The organizer can register a new event.
- The organizer can view event data.
- The organizer can view the list of participants.
- The participant can register for an event.
- The participant can view their registration badge.
- The participant can check-in to the event.

### Business Rules

- The participant can only register for an event once.
- The participant can only register for events with available slots.
- The participant can only check-in to an event once.

### Non-Functional Requirements

- Check-in to the event will be done through a QR code.

### Technologies Used

- Framework: Spring
- Database: HSQLDB
