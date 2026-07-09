Stage 7: Check local config

Run this command:

Get-ChildItem src\resources

Then run:

Get-Content src\resources\config-local.yml

If it shows secrets/tokens, hide them before sharing screenshot.

Stage 8: Check middleware part in app.py

Run:

Get-Content app.py | Select-Object -Skip 80 -First 30

We need to see this part:

app.add_middleware(BearerAuthMiddleware)
Stage 9: Check if app has local bypass already

Run:

Select-String -Path app.py,src\resources\config-local.yml -Pattern "local|auth|BearerAuthMiddleware|APP_ENV|DEVELOPMENT|JWT|jwk|audience|middleware" -CaseSensitive:$false

Do only these 3 commands now:

Get-ChildItem src\resources
Get-Content src\resources\config-local.yml
Get-Content app.py | Select-Object -Skip 80 -First 30

Send me the output. Then I’ll tell you whether to use JWT token or add safe local bypass.






The local app setup is now successful; the next milestone is authentication access for protected endpoints, followed by AlphaSense OBO integration and query-response testing.
