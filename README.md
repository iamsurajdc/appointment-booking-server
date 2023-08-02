# Appointment-Booking-Server

<!-- PROJECT LOGO -->
<br />

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>About the Project</li>
    <li>Built with</li>
    <li>Getting started</li>
    <li>Prerequisites</li>
    <li>List of APIs</li>
    <li>Contribute</li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->

## About The Project

This is an application made a part of a module to make appointment booking between people a lot easier. The usual process is to exchange mails between people till they find a convenient time. But this application can skip this process and book appointment.

### Built With

This web application uses the following technology

- [NodeJS](https://nodejs.org)
- [ExpressJS](https://expressjs.com/)
- [Axios](https://www.npmjs.com/package/axios)
- [Firebase](https://firebase.google.com/)

<!-- GETTING STARTED -->

## Getting Started

To preview this application online click here [google.com/](googe.com/)

To run this application locally 2. Clone the repo

```sh
git clone git@github.com:iamsurajdc/appointment-booking-server.git
```

3. Install NPM packages in client directory and server directory
   ```sh
   npm install
   npm start
   ```
4. Create a firebase firestore database with collection name `event`
5. Add your firebase service account API key in `serviceAccountKey.json`

### Prerequisites

You need to have the following Prerequisite to get started

- NodeJS
- Firebase Account

## List of APIs

| API Routes   | Parameters         | Description                                                                                                                                                                                                          |
| ------------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| /freeSlots   | Date, Timezone     | Return all the free slots available for a given date converted to whatever timezone we pass.                                                                                                                         |
| /createEvent | DateTime, Duration | All the data passed will create the event and store that into the firestore document, if the event already exists for that time you need to return status code 422 or else just store it and return with status 200. |
| /getEvents   | startDate, endDate | Return all the events between given StartDate & EndDate                                                                                                                                                              |

<!-- CONTRIBUTING -->

## Contributing

You can contribute by following the below steps.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b <feat/something>`)
3. Commit your Changes (`git commit -m 'Added some feature'`)
4. Push to the Branch (`git push origin feat/something`)
5. Open a Pull Request