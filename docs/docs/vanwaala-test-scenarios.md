 VanWaala Test Scenarios
1. Registration, Sign-in and Profile

| ID | Test Scenario | Type |
|---|---|---|
| TS-001 | Register with valid customer information | Positive |
| TS-002 | Register with invalid email format | Negative |
| TS-003 | Register with an already registered email | Negative |
| TS-004 | Register with missing required fields | Negative |
| TS-005 | Register with minimum valid input values | Boundary |
| TS-006 | Register with maximum allowed input values | Boundary |
| TS-007 | Sign in with valid credentials | Positive |
| TS-008 | Sign in with incorrect password | Negative |
| TS-009 | Sign in with unregistered email | Negative |
| TS-010 | Complete profile after registration | Positive |

2. Provider Service Management

| ID | Test Scenario | Type |
|---|---|---|
| TS-011 | Provider creates a service with valid information | Positive |
| TS-012 | Provider creates a service with missing required fields | Negative |
| TS-013 | Provider edits an existing service | Positive |
| TS-014 | Provider deletes an existing service | Positive |
| TS-015 | Unauthorized customer attempts to create a service | Negative |
| TS-016 | Provider submits invalid service information | Negative |
| TS-017 | Provider views created service details | Positive |
| TS-018 | Provider updates service information | Positive |
| TS-019 | Provider attempts to edit unavailable service | Negative |
| TS-020 | Provider cancels service deletion action | Positive |

3. Customer Search and Service Details

| ID | Test Scenario | Type |
|---|---|---|
| TS-021 | Customer searches for an available service | Positive |
| TS-022 | Customer searches with no matching results | Negative |
| TS-023 | Customer searches using valid route information | Positive |
| TS-024 | Customer opens service details | Positive |
| TS-025 | Customer searches with empty input | Negative |
| TS-026 | Customer searches with incomplete information | Negative |
| TS-027 | Customer views provider information | Positive |
| TS-028 | Customer views available seats | Positive |
| TS-029 | Customer refreshes service search results | Positive |
| TS-030 | Customer navigates back from service details | Positive |

4. Seat Requests

| ID | Test Scenario | Type |
|---|---|---|
| TS-031 | Customer requests an available seat | Positive |
| TS-032 | Customer requests a seat when no seats are available | Negative |
| TS-033 | Customer submits duplicate seat request | Negative |
| TS-034 | Customer views pending seat request | State Transition |
| TS-035 | Provider accepts a pending seat request | State Transition |
| TS-036 | Provider rejects a pending seat request | State Transition |
| TS-037 | Customer observes accepted request status | State Transition |
| TS-038 | Customer observes rejected request status | State Transition |
| TS-039 | Unauthorized user attempts to manage another user's request | Negative |
| TS-040 | Failed seat request does not incorrectly reduce available seats | Negative |

5. Authorization

| ID | Test Scenario | Type |
|---|---|---|
| TS-041 | Customer accesses customer-only functionality | Positive |
| TS-042 | Provider accesses provider-only functionality | Positive |
| TS-043 | Customer attempts provider-only action | Negative |
| TS-044 | Provider attempts customer-only action | Negative |
| TS-045 | Unauthenticated user accesses protected feature | Negative |
| TS-046 | User attempts to access another user's data | Negative |
| TS-047 | User session expires while accessing protected feature | Negative |
| TS-048 | User signs out and attempts protected action | Negative |
| TS-049 | Authorized user updates own information | Positive |
| TS-050 | Unauthorized user attempts to modify restricted information | Negative |

6. Bookings and Notifications

| ID | Test Scenario | Type |
|---|---|---|
| TS-051 | Booking is created after accepted seat request | Positive |
| TS-052 | Booking is not created after rejected request | Negative |
| TS-053 | Customer views booking details | Positive |
| TS-054 | Provider views booking information | Positive |
| TS-055 | Customer receives notification after request acceptance | Positive |
| TS-056 | Customer receives notification after request rejection | Positive |
| TS-057 | Notification reflects the correct request status | Positive |
| TS-058 | Duplicate notification is not generated for one status change | Negative |
| TS-059 | Booking information remains available after refresh | Positive |
| TS-060 | Unauthorized user attempts to view another user's booking | Negative |

7. Route Tracking

| ID | Test Scenario | Type |
|---|---|---|
| TS-061 | Provider starts route tracking | Positive |
| TS-062 | Provider stops route tracking | Positive |
| TS-063 | Customer cannot see location before tracking starts | Negative |
| TS-064 | Customer sees intended tracking information after tracking starts | Positive |
| TS-065 | Customer no longer sees active tracking after tracking stops | State Transition |
| TS-066 | Unauthorized user attempts to access tracking information | Negative |
| TS-067 | Provider starts tracking with valid route | Positive |
| TS-068 | Provider attempts invalid tracking action | Negative |
| TS-069 | Tracking state remains correct after refresh | State Transition |
| TS-070 | Tracking information updates while route is active | Positive |

8. Paywall and Subscription

| ID | Test Scenario | Type |
|---|---|---|
| TS-071 | User with active subscription accesses paid feature | Positive |
| TS-072 | User without subscription sees paywall | Positive |
| TS-073 | User attempts restricted feature without subscription | Negative |
| TS-074 | Subscription status is displayed correctly | Positive |
| TS-075 | User accesses feature after subscription activation | State Transition |
| TS-076 | Expired subscription restricts paid feature | Negative |
| TS-077 | User refreshes page after subscription change | State Transition |
| TS-078 | Unauthorized user attempts subscription-related action | Negative |
| TS-079 | Subscription information remains consistent across sessions | Positive |
| TS-080 | User navigates away from paywall and returns | Positive |

9. End-to-End Customer Journey

| ID | Test Scenario | Type |
|---|---|---|
| TS-081 | Customer registers and completes profile | End-to-End |
| TS-082 | Customer searches for a service after registration | End-to-End |
| TS-083 | Customer views service details | End-to-End |
| TS-084 | Customer requests an available seat | End-to-End |
| TS-085 | Customer observes pending request | End-to-End |
| TS-086 | Customer observes accepted request | End-to-End |
| TS-087 | Customer observes rejected request | End-to-End |
| TS-088 | Customer views resulting booking state | End-to-End |
| TS-089 | Customer observes route tracking visibility | End-to-End |
| TS-090 | Customer verifies final service/request state | End-to-End |

10. End-to-End Provider Journey

| ID | Test Scenario | Type |
|---|---|---|
| TS-091 | Provider registers and completes profile | End-to-End |
| TS-092 | Provider creates a service | End-to-End |
| TS-093 | Provider edits a service | End-to-End |
| TS-094 | Provider receives a seat request | End-to-End |
| TS-095 | Provider accepts a seat request | End-to-End |
| TS-096 | Provider rejects a seat request | End-to-End |
| TS-097 | Provider observes updated request state | End-to-End |
| TS-098 | Provider starts route tracking | End-to-End |
| TS-099 | Provider observes active tracking state | End-to-End |
| TS-100 | Provider stops route tracking | End-to-End |
