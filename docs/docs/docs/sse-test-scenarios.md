# CallSignGPT SSE Test Scenarios

| ID | Scenario | Type | Priority |
|---|---|---|---|
| SSE-001 | Response text appears progressively | Positive | Critical |
| SSE-002 | Streaming chunks remain in correct order | Positive | Critical |
| SSE-003 | Streaming chunks are not duplicated | Negative | Critical |
| SSE-004 | Final response remains stable after completion | Positive | Critical |
| SSE-005 | Refresh during generation behaves predictably | State Transition | High |
| SSE-006 | Concurrent action during generation behaves predictably | Concurrency | High |
| SSE-007 | Upstream failure shows controlled error | Negative | Critical |
| SSE-008 | Failed stream does not remain permanently loading | Recovery | Critical |
| SSE-009 | Markdown remains readable during/after streaming | Positive | High |
| SSE-010 | Code remains readable during/after streaming | Positive | High |
| SSE-011 | Completed response is stored in conversation history | Positive | Critical |
| SSE-012 | Stream completion is detected correctly | Positive | High |
| SSE-013 | Network interruption during streaming is handled | Negative | Critical |
| SSE-014 | Network recovery allows expected subsequent action | Recovery | High |
| SSE-015 | Rapid sends do not corrupt streamed responses | Concurrency | Critical |
