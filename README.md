Stage 6: Create one test session

Important: Do not close the server terminal.
Open a new terminal in VS Code.

Run this command in the new terminal:

Invoke-RestMethod -Method POST "http://localhost:8081/apps/base_llm_agent/users/test-user/sessions" `
  -ContentType "application/json" `
  -Body '{"state":{}}'

Expected result: it should return session details, maybe with an id or session_id.

If it works, then run this to list sessions:

Invoke-RestMethod -Method GET "http://localhost:8081/apps/base_llm_agent/users/test-user/sessions"
Do only this now

Run:

Invoke-RestMethod -Method POST "http://localhost:8081/apps/base_llm_agent/users/test-user/sessions" `
  -ContentType "application/json" `
  -Body '{"state":{}}'

Send me the output.
After session is created, we will test /run.
