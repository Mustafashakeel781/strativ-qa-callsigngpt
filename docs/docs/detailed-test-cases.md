# CallSignGPT Detailed Test Cases

## TC-001 — Login with valid credentials

- Priority: Critical
- Test Type: Positive
- Preconditions: A valid test account exists.
- Test Data: Valid email and password.
- Steps:
  1. Open CallSignGPT.
  2. Enter valid email.
  3. Enter valid password.
  4. Click Login.
- Expected Result: User is authenticated and the chat interface is displayed.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-002 — Login with incorrect password

- Priority: High
- Test Type: Negative
- Preconditions: A registered test account exists.
- Test Data: Valid email and incorrect password.
- Steps:
  1. Open the login page.
  2. Enter the registered email.
  3. Enter an incorrect password.
  4. Submit the form.
- Expected Result: Login is rejected and an appropriate error is displayed.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-003 — Register with valid information

- Priority: High
- Test Type: Positive
- Preconditions: Registration is available.
- Test Data: Valid synthetic registration information.
- Steps:
  1. Open registration.
  2. Enter valid required information.
  3. Submit the form.
- Expected Result: Account registration completes successfully.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-004 — Register with invalid email

- Priority: High
- Test Type: Negative
- Preconditions: Registration page is available.
- Test Data: Invalid email format.
- Steps:
  1. Open registration.
  2. Enter otherwise valid information.
  3. Enter an invalid email.
  4. Submit.
- Expected Result: Registration is rejected and email validation is shown.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-005 — Register with missing required fields

- Priority: High
- Test Type: Negative
- Preconditions: Registration page is available.
- Test Data: Required fields left empty.
- Steps:
  1. Open registration.
  2. Leave required fields empty.
  3. Submit the form.
- Expected Result: Required-field validation is displayed.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-006 — Send valid chat message

- Priority: Critical
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: Valid short message.
- Steps:
  1. Open a conversation.
  2. Enter a valid message.
  3. Send the message.
- Expected Result: Message is accepted and an AI response is generated.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-007 — Send empty message

- Priority: High
- Test Type: Negative
- Preconditions: User is logged in.
- Test Data: Empty input.
- Steps:
  1. Open chat.
  2. Leave the input empty.
  3. Attempt to send.
- Expected Result: Empty message is not submitted.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-008 — Send whitespace-only message

- Priority: High
- Test Type: Negative
- Preconditions: User is logged in.
- Test Data: Spaces only.
- Steps:
  1. Open chat.
  2. Enter whitespace characters.
  3. Send the message.
- Expected Result: Whitespace-only input is rejected.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-009 — Send message at maximum allowed length

- Priority: High
- Test Type: Boundary
- Preconditions: Approved maximum message length is known.
- Test Data: Message at the maximum allowed length.
- Steps:
  1. Open chat.
  2. Enter a message at the approved maximum.
  3. Send.
- Expected Result: Message is accepted if it meets the approved limit.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-010 — Send message above maximum length

- Priority: High
- Test Type: Boundary
- Preconditions: Approved maximum message length is known.
- Test Data: Message exceeding the approved limit.
- Steps:
  1. Open chat.
  2. Enter a message above the limit.
  3. Attempt to send.
- Expected Result: Input is rejected or appropriately limited.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-011 — Start new conversation

- Priority: High
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: None.
- Steps:
  1. Open the chat interface.
  2. Select new conversation.
- Expected Result: A new conversation is created.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-012 — Switch conversations

- Priority: High
- Test Type: Positive
- Preconditions: Multiple conversations exist.
- Test Data: Two test conversations.
- Steps:
  1. Open conversation A.
  2. Switch to conversation B.
  3. Return to conversation A.
- Expected Result: Correct conversation content is displayed each time.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-013 — Refresh after completed response

- Priority: High
- Test Type: State Transition
- Preconditions: A response has completed.
- Test Data: Completed test conversation.
- Steps:
  1. Send a valid message.
  2. Wait for completion.
  3. Refresh the page.
- Expected Result: Completed conversation remains available as expected.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-014 — Network interruption during message send

- Priority: Critical
- Test Type: Negative
- Preconditions: User is logged in.
- Test Data: Valid message.
- Steps:
  1. Enter a valid message.
  2. Interrupt network connectivity during submission.
- Expected Result: Application handles the failure without remaining permanently stuck.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-015 — Recover after network interruption

- Priority: High
- Test Type: Recovery
- Preconditions: Network interruption has occurred.
- Test Data: Valid message.
- Steps:
  1. Restore network connectivity.
  2. Retry the message.
- Expected Result: Application recovers and allows the expected action.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-016 — Server error handling

- Priority: Critical
- Test Type: Negative
- Preconditions: Test environment can produce a controlled server error.
- Test Data: Valid request.
- Steps:
  1. Submit a valid message.
  2. Trigger the approved server-error condition.
- Expected Result: Controlled error is displayed and permanent loading does not occur.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-017 — Logout successfully

- Priority: Critical
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: Valid account.
- Steps:
  1. Open account controls.
  2. Select logout.
- Expected Result: User is logged out.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-018 — Protected access after logout

- Priority: Critical
- Test Type: Security
- Preconditions: User has logged out.
- Test Data: None.
- Steps:
  1. Log out.
  2. Attempt to access protected chat functionality.
- Expected Result: Protected functionality is not accessible.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-019 — Markdown readability

- Priority: High
- Test Type: Positive
- Preconditions: User can send chat messages.
- Test Data: Prompt requesting Markdown formatting.
- Steps:
  1. Send a formatting request.
  2. Review the generated response.
- Expected Result: Markdown content is readable and correctly displayed.
- Actual Result: To be recorded during execution.
- Status: Not Executed

## TC-020 — Code block readability

- Priority: High
- Test Type: Positive
- Preconditions: User is logged in.
- Test Data: Prompt requesting a code example.
- Steps:
  1. Request a code example.
  2. Review the response.
- Expected Result: Code is displayed in a readable code block.
- Actual Result: To be recorded during execution.
- Status: Not Executed
