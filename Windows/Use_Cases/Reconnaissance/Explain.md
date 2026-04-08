Attacker / User
      │
      │  Runs recon commands (ping, nslookup, netstat, etc.)
      ▼
Windows Machine (Sysmon Enabled)
      │
      │  Sysmon Event ID 1 (Process Creation)
      ▼
Windows Event Log (Sysmon Operational Channel)
      │
      │  AMA Agent / Log Forwarding
      ▼
Log Analytics Workspace
      │
      │  KQL Analytic Rule
      ▼
┌──────────────────────────────────────────────┐
│ 1. Filter last 15 mins                       │
│ 2. Select Sysmon Process Creation (EventID 1)│
│ 3. Extract CommandLine → ProcessName         │
│ 4. Match recon tools                         │
│ 5. Count executions per host                 │
│ 6. Threshold >= 3                            │
└──────────────────────────────────────────────┘
      │
      ▼
Microsoft Sentinel Alert
      │
      ▼
SOC Investigation (Recon Activity)