VanWaala Exploratory Testing
Session 1 — Form Validation and Recovery
Charter
Explore registration and profile forms to identify validation, input-handling and recovery issues.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Valid registration data

Invalid email

Empty fields

Invalid/short values

Boundary-length values

Areas Covered

Customer registration

Provider registration

Profile completion

Required fields

Invalid input handling

Error messages

Variations Attempted

Empty fields

Invalid email format

Short input

Long input

Correcting invalid data after an error

Submitting forms multiple times

Questions

Are required fields clearly identified?

Are validation messages understandable?

Can the user recover after entering invalid data?

Does valid data submit successfully after correcting an error?

Findings

No major validation defects observed during form submission tests.

Areas Not Covered

Payment flows

Route tracking

API behaviour

Session 2 — Navigation and State Persistence
Charter
Explore navigation and verify whether important application state remains consistent while moving between pages.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Test customer account

Test provider account

Existing service

Existing seat request

Areas Covered

Page navigation

Back and forward navigation

Profile state

Service details

Seat request state

Page refresh

Variations Attempted

Navigate forward and backward

Refresh pages

Open and close service details

Return to a previous page

Navigate between profile and service pages

Questions

Is the user's state preserved after navigation?

Does refresh change the current state?

Are previously entered or selected values retained?

Does browser back navigation behave correctly?

Findings

Application correctly preserved route and session state across back/forward navigation and page refresh.

Areas Not Covered

Network interruption

Payment flows

API testing

Session 3 — Changing Network Behaviour
Charter
Explore application behaviour when network conditions become slow or unavailable.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Valid customer account

Valid provider account

Existing service

Seat request data

Areas Covered

Registration

Service search

Seat requests

Page loading

Error recovery

Variations Attempted

Normal network

Slow network

Temporary network interruption

Retry after failure

Refresh after network recovery

Questions

Does the application show a useful error?

Does loading continue indefinitely?

Is data submitted more than once after retrying?

Can the user recover after the connection returns?

Findings

Application handles offline reconnect gracefully without duplicating seat requests.

Areas Not Covered

Payment

AI features

Mobile application testing

Session 4 — Seat Request State Exploration
Charter
Explore the complete seat-request workflow and verify state changes between customer and provider.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Customer account

Provider account

Service with available seats

Service with limited availability

Areas Covered

Seat request creation

Pending state

Acceptance

Rejection

Booking state

Available seat count

Variations Attempted

Request one available seat

Request multiple seats

Submit duplicate request

Provider accepts request

Provider rejects request

Refresh after state change

Questions

Is the pending state displayed correctly?

Does acceptance update the customer state?

Does rejection update the customer state?

Does available seat information remain correct?

Are duplicate requests prevented?

Findings

Seat availability correctly decremented upon request acceptance and preserved status.

Areas Not Covered

Route tracking

Payment

API testing

Session 5 — Authorization and Role Exploration
Charter
Explore access control between Customer and Provider roles.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Customer account

Provider account

Customer-owned data

Provider-owned service

Areas Covered

Customer permissions

Provider permissions

Protected pages

Service management

Profile access

Unauthorized actions

Variations Attempted

Customer attempts provider action

Provider attempts customer action

Access protected page while logged out

Access another user's data

Sign out and use browser back navigation

Refresh protected page

Questions

Are role permissions enforced?

Can a user access another user's data?

Are protected pages inaccessible after logout?

Does browser navigation bypass authorization?

Findings

Unauthorized direct URL access attempts correctly redirected to login or access denied page.

Areas Not Covered

Payment

Route tracking

Mobile-specific behaviour

Session 6 — Route Tracking Exploration
Charter
Explore route tracking visibility and verify that location information is shown only under the intended conditions.

Build / Environment

Product: VanWaala

Environment: Training environment

Browser: Chrome

Device: Desktop

Date: 16-Sep-2026

Test Data

Provider account

Customer account

Active service

Test route

Areas Covered

Starting route tracking

Active tracking

Customer visibility

Stopping tracking

Tracking state after refresh

Variations Attempted

Start tracking

View tracking as customer

Refresh during active tracking

Stop tracking

Refresh after stopping

Attempt tracking access without authorization

Questions

Is location hidden before tracking starts?

Does tracking become visible when expected?

Does location stop being visible after tracking stops?

Is tracking state preserved correctly after refresh?

Can unauthorized users access tracking information?

Findings

Live location tracking hidden prior to activation and terminates correctly upon stopping route.

Areas Not Covered

Payment

Subscription

API testing
