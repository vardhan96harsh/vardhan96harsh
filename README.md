Stage 13: Create session again

Keep this server terminal open.

Open new terminal and run:

Invoke-RestMethod -Method POST "http://localhost:8081/apps/base_llm_agent/users/test-user/sessions" `
  -ContentType "application/json" `
  -Body '{"state":{}}'

If it works, you should get session data.

After that, run:

Invoke-RestMethod -Method GET "http://localhost:8081/apps/base_llm_agent/users/test-user/sessions"
Send me output

Run the POST command first and send me the output.
If i
