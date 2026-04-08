Attacker Machine
      │
      │  Multiple SSH failed login attempts
      ▼
Linux Target VM (sshd)
      │
      │  Failed password events
      ▼
/var/log/auth.log or Syslog
      │
      │  Syslog Connector / AMA Agent
      ▼
Log Analytics Workspace
      │
      │  KQL Analytic Rule
      ▼
┌──────────────────────────────────────────┐
│ 1. Filter last 15 mins                   │
│ 2. Match sshd failed password events     │
│ 3. Parse source IP + port                │
│ 4. Group by IP + host                    │
│ 5. Count failed attempts                 │
│ 6. Threshold >= 10                       │
└──────────────────────────────────────────┘
      │
      ▼
Microsoft Sentinel Alert
      │
      ▼
SOC Investigation / Incident