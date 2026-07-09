gc .env | ? { $_ -match '^\s*[^#].*=' } | % { $p = $_ -split '=',2; Set-Item -Path ("Env:" + $p[0].Trim()) -Value $p[1].Trim() }





$names = @("CONVEYOR_INJECTED_MANAGED_VAULT_URL","CONVEYOR_INJECTED_MANAGED_VAULT_NAMESPACE","CONVEYOR_INJECTED_MANAGED_VAULT_ROLE_ID","CONVEYOR_INJECTED_MANAGED_VAULT_SECRET_ID","ALPHASENSE_API_KEY","ALPHASENSE_EMAIL","ALPHASENSE_PASSWORD","ALPHASENSE_CLIENT_ID","ALPHASENSE_CLIENT_SECRET"); foreach ($n in $names) { "$n set? " + (Test-Path ("Env:" + $n)) }
