# VanWaala Test Scenarios

## 1. Registration and Profile

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-001 | Register with valid customer information | High | Positive |
| TS-002 | Register with invalid phone number | High | Negative |
| TS-003 | Register with an already registered phone number | High | Negative |
| TS-004 | Submit registration with empty required fields | High | Negative |
| TS-005 | Enter an incorrect verification code | High | Negative |
| TS-006 | Enter an expired verification code | Medium | Negative |
| TS-007 | Register with a valid verification code | High | Positive |
| TS-008 | Create a password meeting the required rules | High | Positive |
| TS-009 | Enter an invalid password | High | Negative |
| TS-010 | Complete customer profile with valid information | High | Positive |
| TS-011 | Submit profile with missing required information | High | Negative |
| TS-012 | Enter invalid profile information | Medium | Negative |
| TS-013 | Register as a provider with valid information | High | Positive |
| TS-014 | Provider registration with invalid information | High | Negative |
| TS-015 | Provider completes profile successfully | High | Positive |

## 2. Provider Service Management

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-016 | Provider creates a service with valid information | High | Positive |
| TS-017 | Provider creates a service with missing required fields | High | Negative |
| TS-018 | Provider enters invalid service information | High | Negative |
| TS-019 | Provider sets valid route information | High | Positive |
| TS-020 | Provider sets invalid route information | Medium | Negative |
| TS-021 | Provider sets available seats for a service | High | Positive |
| TS-022 | Provider enters an invalid seat count | High | Boundary |
| TS-023 | Provider edits an existing service | High | Positive |
| TS-024 | Provider deletes an existing service | High | Positive |
| TS-025 | Provider attempts to edit a service they do not own | High | Negative |

## 3. Customer Search and Service Details

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-026 | Customer searches for an available service | High | Positive |
| TS-027 | Customer searches with valid pickup location | High | Positive |
| TS-028 | Customer searches with valid destination | High | Positive |
| TS-029 | Customer searches with no matching results | Medium | Negative |
| TS-030 | Customer searches with empty search fields | Medium | Negative |
| TS-031 | Customer views service details | High | Positive |
| TS-032 | Customer views provider information | Medium | Positive |
| TS-033 | Customer opens an unavailable service | Medium | Negative |
| TS-034 | Customer searches using different route criteria | Medium | Positive |
| TS-035 | Search results display relevant services | High | Positive |

## 4. Seat Requests

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-036 | Customer requests an available seat | High | Positive |
| TS-037 | Customer requests a seat when no seats are available | High | Negative |
| TS-038 | Customer submits a seat request with valid information | High | Positive |
| TS-039 | Customer attempts duplicate seat request | High | Negative |
| TS-040 | Customer views pending seat request | High | State Transition |
| TS-041 | Provider accepts a pending seat request | High | State Transition |
| TS-042 | Provider rejects a pending seat request | High | State Transition |
| TS-043 | Customer observes accepted request status | High | State Transition |
| TS-044 | Customer observes rejected request status | High | State Transition |
| TS-045 | Seat availability updates after acceptance | High | State Transition |
| TS-046 | Failed seat request does not incorrectly reduce seats | High | Negative |
| TS-047 | Customer attempts to request beyond available seats | High | Boundary |
| TS-048 | Customer views existing seat requests | Medium | Positive |
| TS-049 | Provider views pending seat requests | High | Positive |
| TS-050 | Provider handles multiple seat requests | High | State Transition |

## 5. Authorization

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-051 | Customer accesses customer functions | High | Positive |
| TS-052 | Provider accesses provider functions | High | Positive |
| TS-053 | Customer attempts to access provider functions | High | Negative |
| TS-054 | Provider attempts unauthorized customer action | High | Negative |
| TS-055 | Unauthenticated user accesses protected functionality | High | Negative |
| TS-056 | User accesses their own profile | High | Positive |
| TS-057 | User attempts to modify another user's information | High | Negative |
| TS-058 | Provider modifies their own service | High | Positive |
| TS-059 | Provider attempts to modify another provider's service | High | Negative |
| TS-060 | Authorization remains correct after login | High | Positive |

## 6. Bookings

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-061 | Booking is created after an accepted seat request | High | Positive |
| TS-062 | Booking is not created for a rejected request | High | Negative |
| TS-063 | Customer views booking details | High | Positive |
| TS-064 | Provider views booking information | High | Positive |
| TS-065 | Booking reflects the correct service | High | Positive |
| TS-066 | Booking reflects the correct customer | High | Positive |
| TS-067 | Booking reflects the correct seat information | High | Positive |
| TS-068 | Customer accesses booking history | Medium | Positive |
| TS-069 | Provider accesses booking information for their service | High | Positive |
| TS-070 | Unauthorized user attempts to access another booking | High | Negative |

## 7. Notifications

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-071 | Customer receives notification after seat acceptance | High | Positive |
| TS-072 | Customer receives notification after seat rejection | High | Positive |
| TS-073 | Provider receives notification for a new seat request | High | Positive |
| TS-074 | Notification contains relevant request information | Medium | Positive |
| TS-075 | Notifications remain available after page navigation | Medium | Positive |
| TS-076 | User views notification list | Medium | Positive |
| TS-077 | Notification status updates appropriately | Medium | State Transition |
| TS-078 | User does not receive unrelated notifications | Medium | Negative |

## 8. Route Tracking

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-079 | Provider starts route tracking | High | Positive |
| TS-080 | Provider stops route tracking | High | Positive |
| TS-081 | Customer cannot see location before tracking starts | High | Negative |
| TS-082 | Customer can see intended tracking information after tracking starts | High | Positive |
| TS-083 | Customer sees tracking state while route is active | High | State Transition |
| TS-084 | Customer no longer sees active tracking after tracking stops | High | State Transition |
| TS-085 | Unauthorized user attempts to access tracking information | High | Negative |
| TS-086 | Provider starts tracking for an active route | High | Positive |
| TS-087 | Provider attempts invalid tracking action | Medium | Negative |
| TS-088 | Tracking state remains consistent after navigation | High | State Transition |

## 9. Subscription / Paywall

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-089 | User accesses a feature without subscription when allowed | Medium | Positive |
| TS-090 | Restricted feature displays paywall when enabled | High | Negative |
| TS-091 | User with valid subscription accesses restricted feature | High | Positive |
| TS-092 | Expired subscription restricts access appropriately | High | State Transition |
| TS-093 | Subscription status is displayed correctly | Medium | Positive |
| TS-094 | User attempts restricted action without required access | High | Negative |

## 10. Cross-Feature and Error Handling

| ID | Scenario | Priority | Type |
|---|---|---|---|
| TS-095 | User session remains valid while navigating between features | High | Positive |
| TS-096 | Expired session prevents access to protected features | High | Negative |
| TS-097 | Network interruption during an important user action is handled correctly | High | Negative |
| TS-098 | Failed operation displays an appropriate error state | High | Negative |
| TS-099 | Page refresh preserves the expected application state | High | State Transition |
| TS-100 | Customer completes registration, discovers a service and submits a seat request | Critical | End-to-End |

## Highest-Risk Scenarios

- **TS-036:** Customer requests an available seat.
- **TS-041:** Provider accepts a pending seat request.
- **TS-047:** Customer attempts to request beyond available seats.
- **TS-053:** Customer attempts to access provider functions.
- **TS-081:** Customer cannot see location before route tracking starts.
- **TS-082:** Customer sees intended tracking information after tracking starts.
- **TS-100:** Complete customer journey from registration to seat request.
