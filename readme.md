# Canis Educere Mock API
---

#### Courtney Phillips
#### March 2023

## Overview

This repo configures a sample RESTful API using Mockend, built with the sole functionality of mocking simple LMS data for use in [Project Canis Educere](https://github.com/courtneyphillips/project-canis-educere).

For more information on Mockend, visit the [Mockend Documentation](https://docs.mockend.com/) and/or their [demo project on GitHub](https://github.com/mockend/demo).

## Mock Data

This basic API is meant to simulate a very simple and rudimentary LMS API. It serves data on Learners, their progress on several fictional certification programs, and the Organizations (ie: employers) they belong to.

Each `Organization` and `Learner` object offers the following values:

```
Organization {
  companyName: "string",
  id: int,
  industrySector: "string",
  accountHealth: "string"
}

Learner {
  email: "string",
  name: "string",
  id: int,
  accountCreation: datetime,
  activeLearningHours: int,
  organizationId: Organization.id,
  roleType: "string",
  kubernetesCertified: ,
  devOpsCertified: "true", "false", "in progress", or "pending exam",
  fundamentalsCertified: "true", "false", "in progress", or "pending exam",
  advancedSkillsCertified: "true", "false", "in progress", or "pending exam",
}
```

## Endpoints

Root endpoints for the `Organization` and `Learner` objects are accessed at the following URLS:

```
https://mockend.com/courtneyphillips/canis-educere-mock-api/organizations
https://mockend.com/courtneyphillips/canis-educere-mock-api/learners
```

As a RESTful API, the following endpoints are available:

```
GET    .../organizations
GET    .../organizations/:id
POST   .../organizations
PUT    .../organizations/:id
PATCH  .../organizations/:id
DELETE .../organizations/:id
```

```
GET    .../learners
GET    .../learners/:id
POST   .../learners
PUT    .../learners/:id
PATCH  .../learners/:id
DELETE .../learners/:id
```

As outlined in the [Query entry of the Mockend Documentation](https://docs.mockend.com/rest#query) resources can be queried with a variety of parameters. (e.g. `.../learners?_limit=5&activeLearningHours_order=desc`)

_**Important Note:** As outlined in the [Mockend Documentation](https://docs.mockend.com/rest), `POST/PUT/PATCH/DELETE` are mocked endpoints and will not alter data. This is expected behavior._

## Tools Used

- [**Mockend**](https://docs.mockend.com/): Installed on this repository, the Mockend service consumes the `.mockend.config.json` file in this repository to scaffold and serve a basic REST API of mock data.
- [**ChatGPT**](https://chat.openai.com/chat/): Used to generate fictional learner and organization names. (e.g.: _"Can you generate me a list of 20 tech company names themed around different animals, formatted as an array of strings?"_)
