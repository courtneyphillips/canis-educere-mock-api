# Canis Educere Mock API

## Description

This repo configures a sample RESTful API using Mockend, built with the sole functionality of mocking simple LMS data for use in [Project Canis Educere](link),

For more information on Mockend, visit their [GitHub Repo]() and/or the [Mockend Documentation]().

## Endpoints

Root endpoints for the `Feedback` and `Course` objects are accessed at the following URLS:

```
https://mockend.com/courtneyphillips/canis-educere-mock-api/feedback
https://mockend.com/courtneyphillips/canis-educere-mock-api/course
```

As a RESTful API, the following endpoints are available:

```
GET    mockend.com/courtneyphillips/canis-educere-mock-api/courses
GET    mockend.com/courtneyphillips/canis-educere-mock-api/courses/:id
POST   mockend.com/courtneyphillips/canis-educere-mock-api/courses
PUT    mockend.com/courtneyphillips/canis-educere-mock-api/courses/:id
PATCH  mockend.com/courtneyphillips/canis-educere-mock-api/courses/:id
DELETE mockend.com/courtneyphillips/canis-educere-mock-api/courses/:id
```

```
GET    mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks
GET    mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks/:id
POST   mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks
PUT    mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks/:id
PATCH  mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks/:id
DELETE mockend.com/courtneyphillips/canis-educere-mock-api/feedbacks/:id
```

**Important Note:** As outlined in the [Mockend Documentation](https://docs.mockend.com/rest), `POST/PUT/PATCH/DELETE` are mocked endpoints and will not alter data. This is expected behavior.

## Tools Used

- **Mockend**: Installed on this repository, the Mockend service consumes the `.mockend.config.json` file present here to serve a sample API.
- **ChatGPT**: Generated fictional course titles and author names used in mock data.
