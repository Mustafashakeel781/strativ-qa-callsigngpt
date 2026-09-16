# CallSignGPT Conventional Test Scenarios

## 1. Registration and Authentication

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-001 | Register with valid information | Positive | High |
| CON-002 | Register with missing required fields | Negative | High |
| CON-003 | Register with invalid email format | Negative | High |
| CON-004 | Register with already registered email | Negative | High |
| CON-005 | Register with invalid password | Negative | High |
| CON-006 | Register with minimum valid input | Boundary | Medium |
| CON-007 | Register with maximum allowed input | Boundary | Medium |
| CON-008 | Login with valid credentials | Positive | Critical |
| CON-009 | Login with incorrect password | Negative | High |
| CON-010 | Login with unregistered account | Negative | High |

## 2. Sessions and Logout

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-011 | User remains signed in during normal navigation | Positive | High |
| CON-012 | User logs out successfully | Positive | Critical |
| CON-013 | Logged-out user accesses protected page | Negative | Critical |
| CON-014 | Session expires during use | State Transition | High |
| CON-015 | User signs in again after session expiry | State Transition | High |
| CON-016 | Refresh page during active session | Positive | High |
| CON-017 | Browser back after logout does not expose protected data | Security | Critical |
| CON-018 | Multiple login attempts are handled correctly | Negative | Medium |
| CON-019 | User closes and reopens browser during session | State Transition | Medium |
| CON-020 | User navigates between authenticated pages | Positive | Medium |

## 3. Chat Input

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-021 | Send valid short message | Positive | Critical |
| CON-022 | Send empty message | Negative | High |
| CON-023 | Send whitespace-only message | Negative | High |
| CON-024 | Send message at minimum allowed length | Boundary | Medium |
| CON-025 | Send message at maximum allowed length | Boundary | High |
| CON-026 | Send message above maximum allowed length | Boundary | High |
| CON-027 | Send message containing numbers | Positive | Low |
| CON-028 | Send message containing special characters | Positive | Medium |
| CON-029 | Send multiple messages sequentially | Positive | High |
| CON-030 | Attempt rapid consecutive sends | Boundary | High |

## 4. Conversations

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-031 | Start a new conversation | Positive | High |
| CON-032 | Send message in a new conversation | Positive | Critical |
| CON-033 | Switch between conversations | Positive | High |
| CON-034 | Conversation history remains available | Positive | High |
| CON-035 | Refresh during conversation | State Transition | High |
| CON-036 | Refresh after completed response | State Transition | High |
| CON-037 | Open an existing conversation | Positive | High |
| CON-038 | Create multiple conversations | Positive | Medium |
| CON-039 | Return to previous conversation | Positive | Medium |
| CON-040 | Conversation state remains consistent after navigation | State Transition | High |

## 5. Network and Recovery

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-041 | Chat works under normal network conditions | Positive | Critical |
| CON-042 | Network interruption during message send | Negative | Critical |
| CON-043 | Network recovers after failed request | Recovery | High |
| CON-044 | User retries after network failure | Recovery | High |
| CON-045 | Network becomes slow during response generation | Negative | High |
| CON-046 | Server error is displayed correctly | Negative | Critical |
| CON-047 | Timeout is handled correctly | Negative | High |
| CON-048 | Failed request does not leave permanent loading state | Recovery | Critical |
| CON-049 | Refresh after network failure | Recovery | High |
| CON-050 | Application remains usable after recovery | Recovery | High |

## 6. Responsive and Browser Behaviour

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-051 | Chat interface works on desktop browser | Positive | High |
| CON-052 | Chat interface works at narrow browser width | Responsive | Medium |
| CON-053 | Navigation works using browser back button | Positive | Medium |
| CON-054 | Navigation works using browser forward button | Positive | Medium |
| CON-055 | Chat input remains accessible after resizing | Responsive | Medium |
| CON-056 | Long response remains readable | Positive | High |
| CON-057 | Markdown content remains readable | Positive | High |
| CON-058 | Code block remains readable | Positive | High |
| CON-059 | Page refresh preserves expected application state | State Transition | High |
| CON-060 | Browser navigation does not expose unauthorized content | Security | Critical |

## 7. Pricing and Account Access

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-061 | User views PKR pricing information | Positive | Medium |
| CON-062 | Account access matches user's subscription state | Positive | High |
| CON-063 | User without required access sees appropriate restriction | Negative | High |
| CON-064 | Subscription status is displayed correctly | Positive | High |
| CON-065 | Access changes after subscription activation | State Transition | High |
| CON-066 | Access changes after subscription expiry | State Transition | High |
| CON-067 | Pricing information is displayed consistently | Positive | Medium |
| CON-068 | Unauthorized user cannot bypass account restrictions | Security | Critical |
| CON-069 | Logout removes access to protected account features | Security | Critical |
| CON-070 | Account access remains correct after refresh | State Transition | High |

## 8. General Chat and Account Behaviour

| ID | Scenario | Type | Priority |
|---|---|---|---|
| CON-071 | User sends a second message after completed response | Positive | High |
| CON-072 | User starts another conversation after completion | Positive | High |
| CON-073 | User switches conversation while response is available | State Transition | High |
| CON-074 | User refreshes after completed conversation | State Transition | High |
| CON-075 | User navigates away and returns to chat | State Transition | Medium |
| CON-076 | Completed response remains in conversation history | Positive | Critical |
| CON-077 | User can continue conversation after previous response | Positive | High |
| CON-078 | User cannot use protected chat after logout | Security | Critical |
| CON-079 | Application recovers after temporary failure | Recovery | High |
| CON-080 | Complete normal chat journey works from login to saved response | End-to-End | Critical |
