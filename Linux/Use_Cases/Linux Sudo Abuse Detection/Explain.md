```
User / Attacker
      │
      │  Attempts sudo with wrong password / unauthorized command
      ▼
Linux Target VM
      │
      │  sudo authentication failure logs
      ▼
/var/log/auth.log / /var/log/secure (Syslog)
      │
      │  AMA Agent / Syslog Connector
      ▼
Log Analytics Workspace
      │
      │  KQL Analytic Rule
      ▼
┌──────────────────────────────────────────────┐
│ 1. Filter last 15 mins                       │
│ 2. Identify sudo-related events              │
│ 3. Detect authentication failures            │
│ 4. Extract username                         │
│ 5. Group by user + host                      │
│ 6. Count failed sudo attempts                │
│ 7. Threshold >= 5                            │
└──────────────────────────────────────────────┘
      │
      ▼
Microsoft Sentinel Alert
      │
      ▼
SOC Investigation (Privilege Escalation Attempt)
```