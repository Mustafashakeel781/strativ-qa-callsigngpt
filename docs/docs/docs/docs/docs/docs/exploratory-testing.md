# CallSignGPT Exploratory Testing

## Session 1 — Authentication and Sessions

### Charter
Explore registration, login, logout and session behaviour.

### Areas Covered
- Registration
- Login
- Logout
- Session persistence
- Session expiry

### Test Data
Synthetic test accounts only.

### Variations
- Valid credentials
- Invalid credentials
- Logout and browser back
- Refresh during session
- Session expiry

### Questions
- Are authentication errors clear?
- Is protected content inaccessible after logout?
- Does session state remain consistent?

### Findings
Record only personally observed findings.

### Areas Not Covered
SSE and AI evaluation.

---

## Session 2 — Chat Input and Recovery

### Charter
Explore chat input validation and recovery behaviour.

### Areas Covered
- Empty input
- Whitespace
- Short input
- Long input
- Rapid sends
- Recovery after errors

### Test Data
Synthetic chat prompts.

### Variations
- Empty message
- Whitespace-only message
- Boundary-length message
- Rapid consecutive sends
- Retry after failure

### Questions
- Are invalid inputs rejected?
- Does the interface recover after an error?
- Can the user continue after recovery?

### Findings
Record only personally observed findings.

### Areas Not Covered
Payments and SSE internals.

---

## Session 3 — Conversation and Navigation

### Charter
Explore conversation switching, refresh and browser navigation.

### Areas Covered
- New conversations
- Existing conversations
- Conversation switching
- Refresh
- Browser back/forward

### Questions
- Is conversation state preserved?
- Does navigation expose incorrect content?
- Does refresh behave predictably?

### Findings
Record only personally observed findings.

### Areas Not Covered
AI-quality evaluation.

---

## Session 4 — Network Behaviour

### Charter
Explore application behaviour under changing network conditions.

### Areas Covered
- Slow network
- Network interruption
- Timeout
- Recovery
- Retry

### Questions
- Is a controlled error shown?
- Does loading terminate?
- Can the user recover?

### Findings
Record only personally observed findings.

### Areas Not Covered
Payment flows.

---

## Session 5 — SSE Streaming

### Charter
Explore progressive response streaming.

### Areas Covered
- Progressive text
- Chunk order
- Duplicate chunks
- Final response
- Refresh during generation
- Concurrent actions

### Questions
- Are chunks ordered?
- Are chunks duplicated?
- Does the final response remain stable?
- Does failure produce a controlled error?

### Findings
Record only personally observed findings.

### Areas Not Covered
Pricing.

---

## Session 6 — AI Response Quality

### Charter
Explore AI responses using the fixed evaluation prompt set.

### Areas Covered
- Factuality
- Relevance
- Instruction following
- Formatting
- Completeness
- Unsupported claims
- Refusal behaviour

### Test Data
The fixed 40-prompt evaluation set.

### Questions
- Does the response follow the requested format?
- Is the answer factually supported?
- Does the model invent information?
- Does it follow multi-step instructions?

### Findings
Record AI-quality observations separately from software defects.

### Areas Not Covered
Payment integration.
