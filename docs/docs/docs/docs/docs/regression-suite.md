# CallSignGPT Regression Test Suite

| ID | Regression Test | Area | Priority |
|---|---|---|---|
| REG-001 | User can register | Authentication | High |
| REG-002 | User can login | Authentication | Critical |
| REG-003 | User can logout | Authentication | Critical |
| REG-004 | Protected access is blocked after logout | Security | Critical |
| REG-005 | Valid chat message can be sent | Chat | Critical |
| REG-006 | Empty message is rejected | Validation | High |
| REG-007 | Whitespace-only message is rejected | Validation | High |
| REG-008 | Maximum allowed message is handled correctly | Boundary | High |
| REG-009 | New conversation can be created | Conversations | High |
| REG-010 | Existing conversation can be opened | Conversations | High |
| REG-011 | Conversations can be switched | Conversations | High |
| REG-012 | Completed response remains in history | Chat | Critical |
| REG-013 | Refresh after completed response behaves correctly | State | High |
| REG-014 | Streaming response appears progressively | SSE | Critical |
| REG-015 | SSE chunks remain ordered | SSE | Critical |
| REG-016 | SSE chunks are not duplicated | SSE | Critical |
| REG-017 | Final streamed response remains stable | SSE | Critical |
| REG-018 | SSE failure produces controlled error | SSE | Critical |
| REG-019 | Network interruption is handled | Recovery | Critical |
| REG-020 | Application recovers after network restoration | Recovery | High |
| REG-021 | Markdown remains readable | UI | High |
| REG-022 | Code blocks remain readable | UI | High |
| REG-023 | Browser navigation behaves correctly | Navigation | Medium |
| REG-024 | Pricing is displayed correctly | Account | Medium |
| REG-025 | Account access follows subscription state | Account | High |
