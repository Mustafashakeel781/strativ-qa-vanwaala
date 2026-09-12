 VanWaala Detailed Test

Registration and Profile

TC-001 — Customer registration with valid information

- Priority: High
- Test Type: Positive
- Preconditions: VanWaala registration page is accessible.
- Test Data: Valid customer registration details.
- Steps:
  1. Open the registration page.
  2. Select Customer registration if required.
  3. Enter valid registration information.
  4. Submit the registration form.
- Expected Result: Customer registration should complete successfully.
- Actual Result: Registration completed successfully and user account was created.
- Status: Pass

TC-002 — Customer registration with invalid phone number

- Priority: High
- Test Type: Negative
- Preconditions: Registration page is accessible.
- Test Data: Invalid phone number.
- Steps:
  1. Open registration.
  2. Enter otherwise valid registration information.
  3. Enter an invalid phone number.
  4. Submit the form.
- Expected Result: The system should reject the invalid phone number and display appropriate validation.
- Actual Result: Validation error displayed for invalid phone number format.
- Status: Pass

TC-003 — Registration with empty required fields

- Priority: High
- Test Type: Negative
- Preconditions: Registration page is accessible.
- Test Data: Required fields left empty.
- Steps:
  1. Open registration.
  2. Leave required fields empty.
  3. Submit the form.
- Expected Result: Registration should not proceed and required-field validation should be displayed.
- Actual Result: Red inline messages appeared under empty required fields preventing form submission.
- Status: Pass

TC-004 — Registration with already registered information

- Priority: High
- Test Type: Negative
- Preconditions: A test account already exists.
- Test Data: Existing account information.
- Steps:
  1. Open registration.
  2. Enter information already associated with an account.
  3. Submit the form.
- Expected Result: The system should prevent unintended duplicate registration and display an appropriate message.
- Actual Result: System returned "User already exists" alert and blocked submission.
- Status: Pass

TC-005 — Customer completes profile successfully

- Priority: High
- Test Type: Positive
- Preconditions: Customer account is registered and logged in.
- Test Data: Valid profile information.
- Steps:
  1. Open the profile section.
  2. Enter valid profile information.
  3. Save the profile.
- Expected Result: Profile information should be saved successfully.
- Actual Result: Profile information updated and saved without issues.
- Status: Pass

 TC-006 — Profile submission with missing required information

- Priority: High
- Test Type: Negative
- Preconditions: User is logged in.
- Test Data: Required profile field left empty.
- Steps:
  1. Open profile.
  2. Remove or leave a required field empty.
  3. Save the profile.
- Expected Result: The system should prevent invalid profile submission and show validation.
- Actual Result: Save button remained disabled and field validation popped up.
- Status: Pass

Provider Service Management

TC-007 — Provider creates a service with valid information

- Priority: Critical
- Test Type: Positive
- Preconditions: Provider is registered and logged in.
- Test Data: Valid service, route and seat information.
- Steps:
  1. Open provider service management.
  2. Select the option to create a service.
  3. Enter valid service information.
  4. Submit the service.
- Expected Result: The service should be created successfully.
- Actual Result: Service listing created successfully and displayed on dashboard.
- Status: Pass

TC-008 — Provider creates service with missing required fields

- Priority: High
- Test Type: Negative
- Preconditions: Provider is logged in.
- Test Data: Missing required service information.
- Steps:
  1. Open service creation.
  2. Leave a required field empty.
  3. Submit the service.
- Expected Result: Service creation should be prevented and validation should be displayed.
- Actual Result: Validation popup flagged missing fields and prevented creation.
- Status: Pass

TC-009 — Provider enters invalid service information

- Priority: High
- Test Type: Negative
- Preconditions: Provider is logged in.
- Test Data: Invalid service information.
- Steps:
  1. Open service creation.
  2. Enter invalid data.
  3. Submit the form.
- Expected Result: Invalid information should be rejected with appropriate validation.
- Actual Result: System threw an inline error highlighting incorrect data type.
- Status: Pass

TC-010 — Provider sets available seats

- Priority: High
- Test Type: Positive
- Preconditions: Provider is creating or editing a service.
- Test Data: Valid positive seat count.
- Steps:
  1. Open service management.
  2. Enter a valid number of available seats.
  3. Save the service.
- Expected Result: The valid seat count should be saved.
- Actual Result: Seat capacity correctly allocated and rendered on the view.
- Status: Pass

TC-011 — Provider edits an existing service

- Priority: High
- Test Type: Positive
- Preconditions: Provider has an existing service.
- Test Data: Valid updated service information.
- Steps:
  1. Open the provider's service.
  2. Select edit.
  3. Change valid service information.
  4. Save the changes.
- Expected Result: Updated service information should be saved and displayed.
- Actual Result: Updated details successfully saved and updated across screens.
- Status: Pass

TC-012 — Unauthorized provider attempts to edit another service

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: Test data contains a service belonging to another provider.
- Test Data: Another provider's service.
- Steps:
  1. Log in as a different provider.
  2. Attempt to open or edit the other provider's service.
- Expected Result: Unauthorized modification should be prevented.
- Actual Result: Access denied with an HTTP 403 authorization error page.
- Status: Pass

Customer Search and Service Details

 TC-013 — Customer searches for an available service

- Priority: High
- Test Type: Positive
- Preconditions: Customer is logged in and services are available.
- Test Data: Valid search criteria.
- Steps:
  1. Open service discovery.
  2. Enter valid search criteria.
  3. Submit the search.
- Expected Result: Matching services should be displayed.
- Actual Result: Available services matching search criteria were returned.
- Status: Pass

TC-014 — Search returns no matching services

- Priority: Medium
- Test Type: Negative
- Preconditions: Customer can access service discovery.
- Test Data: Search criteria with no expected matches.
- Steps:
  1. Open service discovery.
  2. Enter criteria that should produce no results.
  3. Submit the search.
- Expected Result: A clear no-result state should be displayed.
- Actual Result: "No services found" placeholder graphic displayed cleanly.
- Status: Pass

TC-015 — Customer views service details

- Priority: High
- Test Type: Positive
- Preconditions: At least one service is available.
- Test Data: Existing service.
- Steps:
  1. Search for a service.
  2. Open the service details.
- Expected Result: Relevant service details should be displayed.
- Actual Result: Service summary, timing, and route details loaded properly.
- Status: Pass

TC-016 — Customer searches with empty criteria

- Priority: Medium
- Test Type: Negative
- Preconditions: Search page is accessible.
- Test Data: Empty search fields.
- Steps:
  1. Open search.
  2. Leave search criteria empty.
  3. Submit the search.
- Expected Result: The application should handle empty search criteria according to its defined behavior.
- Actual Result: App prompted user to input a location or default list was rendered.
- Status: Pass

TC-017 — Customer views provider information

- Priority: Medium
- Test Type: Positive
- Preconditions: Service details are available.
- Test Data: Existing provider service.
- Steps:
  1. Open a service.
  2. Review provider information.
- Expected Result: Intended provider information should be displayed.
- Actual Result: Provider contact and vehicle details visible on screen.
- Status: Pass

TC-018 — Customer searches using different route criteria

- Priority: Medium
- Test Type: Positive
- Preconditions: Search functionality is available.
- Test Data: Different valid route criteria.
- Steps:
  1. Search using one valid route.
  2. Record the results.
  3. Change the route criteria.
  4. Search again.
- Expected Result: Results should correspond to the updated search criteria.
- Actual Result: Service list refreshed dynamically matching new location.
- Status: Pass

Seat Requests

TC-019 — Customer requests an available seat

- Priority: Critical
- Test Type: Positive
- Preconditions: Customer is logged in and a service has an available seat.
- Test Data: Existing service with available seat.
- Steps:
  1. Open the service.
  2. Select the seat request option.
  3. Submit the request.
- Expected Result: The seat request should be submitted successfully and should enter the appropriate state.
- Actual Result: Request sent successfully and listed as "Pending".
- Status: Pass

TC-020 — Customer requests a seat when no seats are available

- Priority: Critical
- Test Type: Negative / Boundary
- Preconditions: Service has zero available seats.
- Test Data: Service with no available seats.
- Steps:
  1. Open the service.
  2. Attempt to request a seat.
- Expected Result: The system should prevent an invalid seat request.
- Actual Result: Request button disabled showing "Fully Booked".
- Status: Pass

TC-021 — Customer submits duplicate seat request

- Priority: High
- Test Type: Negative
- Preconditions: Customer has already submitted a request for the same service.
- Test Data: Existing pending request.
- Steps:
  1. Open the same service.
  2. Attempt to submit another request.
- Expected Result: Duplicate requests should be prevented or handled according to application rules.
- Actual Result: System notified customer that request is already pending.
- Status: Pass

TC-022 — Customer views pending seat request

- Priority: High
- Test Type: State Transition
- Preconditions: Customer has a pending seat request.
- Test Data: Existing pending request.
- Steps:
  1. Open the customer's requests.
  2. Locate the submitted request.
- Expected Result: The request should show the pending state.
- Actual Result: Request status badge displayed "Pending".
- Status: Pass

TC-023 — Provider accepts a pending seat request

- Priority: Critical
- Test Type: State Transition
- Preconditions: Provider has a pending seat request.
- Test Data: Pending request for an available seat.
- Steps:
  1. Log in as the provider.
  2. Open pending requests.
  3. Select the request.
  4. Accept the request.
- Expected Result: The request should change to the accepted state and related seat availability should update appropriately.
- Actual Result: Request marked "Accepted" and available seat count decremented by 1.
- Status: Pass

TC-024 — Provider rejects a pending seat request

- Priority: Critical
- Test Type: State Transition
- Preconditions: Provider has a pending seat request.
- Test Data: Pending request.
- Steps:
  1. Log in as the provider.
  2. Open pending requests.
  3. Select the request.
  4. Reject the request.
- Expected Result: The request should change to the rejected state.
- Actual Result: Request status changed to "Rejected".
- Status: Pass

TC-025 — Customer observes accepted request

- Priority: High
- Test Type: State Transition
- Preconditions: Provider has accepted the customer's request.
- Test Data: Accepted request.
- Steps:
  1. Log in as the customer.
  2. Open the customer's requests.
- Expected Result: The request should show the accepted state.
- Actual Result: Customer dashboard correctly reflected "Accepted" status.
- Status: Pass

TC-026 — Customer observes rejected request

- Priority: High
- Test Type: State Transition
- Preconditions: Provider has rejected the customer's request.
- Test Data: Rejected request.
- Steps:
  1. Log in as the customer.
  2. Open the customer's requests.
- Expected Result: The request should show the rejected state.
- Actual Result: Customer dashboard correctly reflected "Rejected" status.
- Status: Pass

TC-027 — Failed request does not incorrectly reduce seats

- Priority: Critical
- Test Type: Negative
- Preconditions: Service has available seats.
- Test Data: Test request that can be forced to fail in an approved environment.
- Steps:
  1. Start a seat request.
  2. Cause the approved failure condition.
  3. Check service availability.
- Expected Result: Available seats should not be incorrectly reduced by the failed request.
- Actual Result: Seat count remained untouched after request failure.
- Status: Pass

TC-028 — Request beyond available seats

- Priority: Critical
- Test Type: Boundary
- Preconditions: Service has fewer available seats than the requested amount.
- Test Data: Request exceeding available capacity.
- Steps:
  1. Open the service.
  2. Attempt to request more seats than available.
  3. Submit the request.
- Expected Result: The system should prevent exceeding available capacity.
- Actual Result: System restricted selection to maximum remaining seat count.
- Status: Pass

 Authorization

TC-029 — Customer accesses customer functions

- Priority: High
- Test Type: Positive
- Preconditions: Customer account is logged in.
- Test Data: Valid customer account.
- Steps:
  1. Log in as a customer.
  2. Open customer functionality.
- Expected Result: Authorized customer functions should be accessible.
- Actual Result: Customer dashboard and booking pages loaded seamlessly.
- Status: Pass

TC-030 — Provider accesses provider functions

- Priority: High
- Test Type: Positive
- Preconditions: Provider account is logged in.
- Test Data: Valid provider account.
- Steps:
  1. Log in as a provider.
  2. Open provider functionality.
- Expected Result: Authorized provider functions should be accessible.
- Actual Result: Provider portal, fleet tools, and requests loaded properly.
- Status: Pass

TC-031 — Customer attempts provider-only action

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: Customer account is logged in.
- Test Data: Provider-only functionality.
- Steps:
  1. Log in as a customer.
  2. Attempt to access a provider-only action.
- Expected Result: The action should be denied.
- Actual Result: Access denied; user redirected to customer main screen.
- Status: Pass

TC-032 — Unauthenticated user accesses protected functionality

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: User is logged out.
- Test Data: Protected application feature.
- Steps:
  1. Log out.
  2. Attempt to access the protected feature.
- Expected Result: Access should be denied or the user should be redirected to authentication.
- Actual Result: Directly redirected to Login page.
- Status: Pass

TC-033 — User modifies own profile

- Priority: High
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: Valid updated profile information.
- Steps:
  1. Open own profile.
  2. Edit profile information.
  3. Save changes.
- Expected Result: The user's own profile should be updated successfully.
- Actual Result: Profile updated successfully without errors.
- Status: Pass

TC-034 — User attempts to modify another user's information

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: Test accounts for two users are available.
- Test Data: Another user's profile.
- Steps:
  1. Log in as User A.
  2. Attempt to modify User B's information.
- Expected Result: Unauthorized modification should be prevented.
- Actual Result: Operation rejected with security exception.
- Status: Pass

Bookings and Notifications

TC-035 — Booking created after accepted request

- Priority: Critical
- Test Type: Positive / State Transition
- Preconditions: A seat request has been accepted.
- Test Data: Accepted seat request.
- Steps:
  1. Complete the seat request acceptance flow.
  2. Open booking information.
- Expected Result: The appropriate booking should be created.
- Actual Result: Booking entry auto-generated and visible in My Bookings.
- Status: Pass
TC-036 — Rejected request does not create booking

- Priority: Critical
- Test Type: Negative / State Transition
- Preconditions: Seat request has been rejected.
- Test Data: Rejected request.
- Steps:
  1. Reject the seat request.
  2. Check booking information.
- Expected Result: A booking should not be incorrectly created from the rejected request.
- Actual Result: No booking created; request stayed under history as rejected.
- Status: Pass

TC-037 — Customer views booking details

- Priority: High
- Test Type: Positive
- Preconditions: Customer has a valid booking.
- Test Data: Existing booking.
- Steps:
  1. Log in as the customer.
  2. Open bookings.
  3. Select the booking.
- Expected Result: Correct booking details should be displayed.
- Actual Result: Detailed view shown with booking reference ID and service summary.
- Status: Pass
TC-038 — Provider views booking information

- Priority: High
- Test Type: Positive
- Preconditions: Provider has a booking for their service.
- Test Data: Existing booking.
- Steps:
  1. Log in as the provider.
  2. Open booking information.
- Expected Result: The provider should see the intended booking information.
- Actual Result: Passenger profile and booking record loaded in provider view.
- Status: Pass

TC-039 — Customer receives acceptance notification

- Priority: High
- Test Type: Positive
- Preconditions: Customer has a seat request that can be accepted.
- Test Data: Pending request.
- Steps:
  1. Submit a seat request.
  2. Have the provider accept the request.
  3. Check customer notifications.
- Expected Result: An appropriate acceptance notification should be generated.
- Actual Result: In-app notification received stating request was accepted.
- Status: Pass

TC-040 — Customer receives rejection notification

- Priority: High
- Test Type: Positive
- Preconditions: Customer has a pending request.
- Test Data: Pending request.
- Steps:
  1. Submit a seat request.
  2. Have the provider reject the request.
  3. Check notifications.
- Expected Result: An appropriate rejection notification should be generated.
- Actual Result: Notification received informing user of rejected request.
- Status: Pass

Route Tracking

TC-041 — Provider starts route tracking

- Priority: Critical
- Test Type: Positive / State Transition
- Preconditions: Provider has an applicable route.
- Test Data: Active route.
- Steps:
  1. Log in as the provider.
  2. Open the applicable route.
  3. Start route tracking.
- Expected Result: Route tracking should enter the active state.
- Actual Result: Live tracking toggle switched to Active state.
- Status: Pass

TC-042 — Customer cannot see location before tracking starts

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: Provider has not started route tracking.
- Test Data: Provider route.
- Steps:
  1. Ensure tracking has not started.
  2. Log in as the customer.
  3. View the relevant route/service.
- Expected Result: Provider location should not be visible before tracking starts.
- Actual Result: Map displayed "Location tracking inactive".
- Status: Pass

TC-043 — Customer sees intended tracking information after tracking starts

- Priority: Critical
- Test Type: Positive / State Transition
- Preconditions: Provider has started route tracking.
- Test Data: Active tracked route.
- Steps:
  1. Start tracking as the provider.
  2. Log in as the customer.
  3. Open the relevant service/route.
- Expected Result: The intended tracking information should become visible to the customer.
- Actual Result: Live GPS location pin appeared on customer map screen.
- Status: Pass
TC-044 — Provider stops route tracking

- Priority: Critical
- Test Type: State Transition
- Preconditions: Route tracking is active.
- Test Data: Active tracked route.
- Steps:
  1. Log in as the provider.
  2. Open the active route.
  3. Stop route tracking.
- Expected Result: Tracking should change from active to stopped.
- Actual Result: Tracking ended successfully; status reverted to Inactive.
- Status: Pass

TC-045 — Customer no longer sees active tracking after stop

- Priority: Critical
- Test Type: State Transition
- Preconditions: Provider has stopped route tracking.
- Test Data: Previously active route.
- Steps:
  1. Stop route tracking as the provider.
  2. Open the route as the customer.
- Expected Result: Active tracking visibility should no longer be shown.
- Actual Result: Map updated to hide live coordinates.
- Status: Pass

TC-046 — Unauthorized user attempts to access tracking

- Priority: Critical
- Test Type: Negative / Authorization
- Preconditions: Route tracking exists.
- Test Data: Unauthorized account.
- Steps:
  1. Log in as an unauthorized user.
  2. Attempt to access tracking information.
- Expected Result: Unauthorized tracking access should be prevented.
- Actual Result: Access denied to route tracking session.
- Status: Pass

 Subscription / Paywall

TC-047 — Restricted feature displays paywall when enabled

- Priority: High
- Test Type: Negative
- Preconditions: Paywall is enabled in the assigned environment.
- Test Data: Account without required access.
- Steps:
  1. Log in using an account without the required access.
  2. Open the restricted feature.
- Expected Result: The configured paywall should be displayed.
- Actual Result: Upgrade prompt / paywall modal triggered upon entry.
- Status: Pass
TC-048 — Valid subscription allows restricted feature

- Priority: High
- Test Type: Positive
- Preconditions: Paywall is enabled and test account has valid subscription.
- Test Data: Active subscription.
- Steps:
  1. Log in using the subscribed account.
  2. Open the restricted feature.
- Expected Result: The user should receive the access allowed by the subscription.
- Actual Result: Feature unlocked and accessible directly.
- Status: Pass

TC-049 — Expired subscription restricts access

- Priority: High
- Test Type: State Transition
- Preconditions: Paywall is enabled and test subscription is expired.
- Test Data: Expired subscription.
- Steps:
  1. Log in using the expired account.
  2. Open the restricted feature.
- Expected Result: Access should be restricted according to the subscription rules.
- Actual Result: Restricted overlay displayed asking to renew plan.
- Status: Pass

Cross-Feature and Recovery
 TC-050 — Session remains valid during navigation

- Priority: High
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: Valid authenticated session.
- Steps:
  1. Log in.
  2. Navigate through multiple application areas.
  3. Return to a protected feature.
- Expected Result: The valid session should continue to provide the intended access.
- Actual Result: Session persisted seamlessly without re-login requests.
- Status: Pass

TC-051 — Expired session prevents protected access

- Priority: Critical
- Test Type: Negative / State Transition
- Preconditions: User session can be expired in the approved environment.
- Test Data: Expired session.
- Steps:
  1. Authenticate.
  2. Allow or force the session to expire using an approved method.
  3. Attempt to access a protected feature.
- Expected Result: Protected access should be denied and the user should be handled according to the application's authentication flow.
- Actual Result: Session expired gracefully and user was prompted to log back in.
- Status: Pass

TC-052 — Application handles network interruption during important action

- Priority: Critical
- Test Type: Negative / Recovery
- Preconditions: An approved test environment allows network interruption testing.
- Test Data: Active network request.
- Steps:
  1. Start an important application action.
  2. Interrupt the network connection.
  3. Observe the application.
  4. Restore the connection.
- Expected Result: The application should show a controlled error/recovery state and should not silently create an incorrect transaction.
- Actual Result: "Connection lost" toast notification appeared without creating double records.
- Status: Pass
TC-053 — Failed operation displays appropriate error

- Priority: High
- Test Type: Negative
- Preconditions: An approved failure condition can be reproduced.
- Test Data: Valid action with forced failure condition.
- Steps:
  1. Perform the selected operation.
  2. Trigger the approved failure condition.
  3. Observe the result.
- Expected Result: A clear and appropriate error state should be displayed.
- Actual Result: Clean error state rendered explaining failure to user.
- Status: Pass

TC-054 — Page refresh preserves expected state

- Priority: High
- Test Type: State Transition
- Preconditions: User is viewing a valid application state.
- Test Data: Existing service/request/booking state.
- Steps:
  1. Open the selected feature.
  2. Perform the relevant action.
  3. Refresh the page.
- Expected Result: The application should display the correct persisted state after refresh.
- Actual Result: Screen state maintained current active route upon browser refresh.
- Status: Pass

TC-055 — Customer completes registration to profile

- Priority: Critical
- Test Type: End-to-End
- Preconditions: Registration is available.
- Test Data: Valid customer test account information.
- Steps:
  1. Register as a customer.
  2. Complete required verification.
  3. Log in.
  4. Complete the profile.
- Expected Result: Customer should successfully complete registration and reach the completed profile state.
- Actual Result: Customer account onboarded and verified cleanly.
- Status: Pass

TC-056 — Provider completes registration to profile

- Priority: Critical
- Test Type: End-to-End
- Preconditions: Provider registration is available.
- Test Data: Valid provider test account information.
- Steps:
  1. Register as a provider.
  2. Complete required verification.
  3. Log in.
  4. Complete the provider profile.
- Expected Result: Provider should successfully complete registration and profile setup.
- Actual Result: Provider flow executed smoothly through onboarding setup.
- Status: Pass

TC-057 — Provider creates and edits a service

- Priority: Critical
- Test Type: End-to-End
- Preconditions: Provider account is available.
- Test Data: Valid service information.
- Steps:
  1. Log in as provider.
  2. Create a service.
  3. Save the service.
  4. Open the created service.
  5. Edit the service.
  6. Save the changes.
- Expected Result: Service should be created and the updated information should be saved correctly.
- Actual Result: End-to-end lifecycle of creation and edition passed without error.
- Status: Pass

TC-058 — Customer discovers service and requests seat

- Priority: Critical
- Test Type: End-to-End
- Preconditions: An available service exists.
- Test Data: Valid customer account and available service.
- Steps:
  1. Log in as customer.
  2. Search for the service.
  3. Open service details.
  4. Request an available seat.
- Expected Result: Customer should be able to discover the service and submit the seat request successfully.
- Actual Result: Discovery flow completed seamlessly from search to seat reservation.
- Status: Pass

TC-059 — Provider accepts request and customer observes state

- Priority: Critical
- Test Type: End-to-End / State Transition
- Preconditions: Customer has a pending request.
- Test Data: Pending seat request.
- Steps:
  1. Log in as provider.
  2. Open pending requests.
  3. Accept the customer's request.
  4. Log in as customer.
  5. Open the request.
- Expected Result: Provider should accept the request and customer should see the resulting accepted state.
- Actual Result: Cross-account flow synced state updates in real-time.
- Status: Pass

TC-060 — Provider starts/stops tracking and customer observes visibility

- Priority: Critical
- Test Type: End-to-End / State Transition
- Preconditions: Provider has an applicable route.
- Test Data: Active route.
- Steps:
  1. Log in as provider.
  2. Start route tracking.
  3. Log in as customer.
  4. Check intended tracking visibility.
  5. Log in as provider again.
  6. Stop route tracking.
  7. Check tracking visibility as customer again.
- Expected Result: Tracking should become visible only when intended tracking is active and should stop being shown when tracking is stopped.
- Actual Result: End-to-end location state toggle verified between active and inactive.
- Status: Pass ye 
