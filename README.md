\# Restful Booker API Test Automation with Bruno

# Restful Booker API Test Automation with Bruno

[![Bruno API Tests](https://github.com/NaomiMiyake/restful-booker-bruno/actions/workflows/bruno-api-tests.yml/badge.svg)](https://github.com/NaomiMiyake/restful-booker-bruno/actions/workflows/bruno-api-tests.yml)


> A portfolio project demonstrating API test automation using Bruno.



\## Overview



This repository demonstrates API test automation using Bruno for the Restful Booker API.

The project is designed with reusable API requests and scenario-based test execution, covering both positive and negative test scenarios.



\## Features



\- Scenario-based API testing

\- Reusable request components

\- CRUD operations

\- Authentication

\- Full Update (PUT)

\- Partial Update (PATCH)

\- Negative test scenarios

\- Bruno CLI support



\---



\## Tech Stack



\- Bruno

\- JavaScript

\- Bruno CLI

\- GitHub Actions



\---


## Design

Common API request templates are stored in the project root.

Each scenario folder contains copies of the required requests to keep every scenario self-contained.



\## Project Structure



```text

restful-booker-bruno

│
├── .github

│   └── workflows

│       └── bruno-api-tests.yml
├── README.md
├── opencollection.yml
├── environments
│   └── dev.json
├── S001-Booking-Create-Get-Delete
├── S002-Booking-Get-Negative
├── S003-Booking-Delete-Negative
├── S004-Booking-Full-Update
├── S005-Auth-Invalid-Credentials
├── S006-Booking-Partial-Update
├── S007-Booking-Partial-Update-Negative
├── S008-Booking-Full-Update-Negative
├── S009-Booking-Update-Nonexistent
├── S010-Booking-Delete-Nonexistent
├── API-001 Get booking list.yml
├── API-002 Create booking.yml
├── API-003 Get booking by ID.yml
├── API-004 Auth token.yml
├── API-005 Delete booking.yml
├── API-006 Verify booking deleted.yml
├── API-007 Get nonexistent booking.yml
├── API-008 Delete nonexistent booking.yml
├── API-009 Full update booking (PUT).yml
├── API-010 Partial update booking (PATCH).yml
├── API-011 Reject partial update without authentication (PATCH).yml
├── API-012 Reject full update without authentication.yml
├── API-013 Reject auth with invalid credentials.yml
├── API-014 Update nonexistent booking.yml
└── API-015 Delete nonexistent booking.yml

```



\---



\## Test Scenarios



| Scenario | Description |

|-----------|-------------|

| S001 | Booking lifecycle (Create → Get → Delete) |

| S002 | Get nonexistent booking |

| S003 | Delete nonexistent booking |

| S004 | Full update booking (PUT) |

| S005 | Invalid authentication |

| S006 | Partial update booking (PATCH) |

| S007 | Reject partial update without authentication |

| S008 | Reject full update without authentication |

| S009 | Update nonexistent booking |

| S010 | Delete nonexistent booking |



\---



\## Runtime Variables



The following runtime variables are shared between requests.



| Variable | Description |

|----------|-------------|

| bookingId | Booking ID created during the test |

| token | Authentication token |



\---



\## Environment Variables



| Variable | Description |

|----------|-------------|

| baseurl | Restful Booker API endpoint |

| username | Authentication username |

| password | Authentication password |



\---



\## How to Run



Run all scenarios.



```bash

bru run . --env dev

```



Run a single scenario.



```bash

bru run "S001-Booking-Create-Get-Delete" --env dev

```



\---



\## Current Test Coverage



\- Booking CRUD operations

\- Authentication

\- Full Update (PUT)

\- Partial Update (PATCH)

\- Invalid Authentication

\- Unauthorized Requests

\- Nonexistent Resources

\- Runtime Variable Sharing



\---



\## Future Improvements



\- GitHub Actions

\- HTML Report

\- Data-driven testing

\- Multi-environment support



\## Learning Objectives



This project was created to learn and practice:



\- API test automation with Bruno

\- Scenario-based API testing

\- Runtime variable management

\- Positive and negative test design

\- REST API testing best practices

