# ⚙️ Lightweight Asynchronous Cron Engine & Task Scheduler

A robust background worker thread pool utility built natively in Node.js. This application executes scheduled micro-tasks via precise runtime timestamp offsets, eliminating the structural overhead of third-party cron parsing packages.

## 🛠 Advanced System Design
- **Stateful Time-Drift Management**: Calculates explicit millisecond intervals dynamically inside an active process loop to prevent typical interval-drifting issues.
- **Race Condition Immunity**: Mutates the historical job trace parameter state immediately *before* firing async callback routines to handle concurrency constraints safely.
- **Dynamic Runtime Registration**: Exposes ingestion bindings allowing client threads to spin up custom task tracking parameters dynamically via explicit HTTP routing layers.
- **Unified Fault Isolation**: Wraps decoupled thread logic runs inside independent validation safety filters to keep the entire engine context online if one specific job throws a failure hook.

## 🚀 Deployment & Operational Auditing
1. **Initialize Dependencies**:
   ```bash
   npm install express
   ```
2. **Start Scheduler Runtime**:
   ```bash
   node server.js
   ```
3. **Register Dynamic Daemon Payload**:
   Inject a new task with a custom execution frequency runtime variable:
   ```bash
   curl -X POST http://localhost:3000/api/schedule \
     -H "Content-Type: application/json" \
     -d '{"jobId": "payment_sync", "intervalSec": 5}'
   ```
4. **Inspect Tracking Telemetry**:
   Monitor remaining delta execution time counts via the structural metrics dashboard: `http://localhost:3000/api/scheduler/diagnostics`

## ⚙️ Engineering Principles Behind the Code
Relying on external libraries for trivial system scheduling scripts bloats project dependency trees and introduces potential supply-chain vulnerabilities. Building an explicit, decoupled, Map-based tracking state collection allows you to maintain exact processing bounds cleanly using native asynchronous architecture mechanisms.

## License
MIT
