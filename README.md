# Timestamp Microservice

A small Express API that converts dates to Unix timestamps (milliseconds) and UTC strings.

Built for the freeCodeCamp Back-End Development and APIs lab "Build a Timestamp Microservice".

## Run it

```bash
npm install
npm start
```

The server listens on port `8000`.

## API

`GET /api/:date?`

| Request                    | Response                                                       |
| -------------------------- | -------------------------------------------------------------- |
| `/api/2015-12-25`          | `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }` |
| `/api/1451001600000`       | `{ "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }` |
| `/api/05 October 2011`     | any date string `new Date()` can parse                         |
| `/api`                     | the current time                                               |
| `/api/this-is-not-a-date`  | `{ "error": "Invalid Date" }`                                  |
