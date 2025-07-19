Horizon + Tundra + Spool + StubFS + Aurora form a full enterprise-grade HSM stack:

* Tiered storage
* Transparent recall
* Tape backend
* User self-service
* Policy + scheduler

Embedding metadata analysis in **Permafrost** enables:

* **Recall prediction** (hot paths, user patterns)
* **Retention policy tuning**
* **Anomaly detection** (unusual accesses, security triggers)
* **Usage stats for costing or quotas**

Not just a passive bot into an **intelligent HSM engine**.

Permafrost can ingest domain-specific metadata:

* Genomics: sample ID, instrument, run date
* Imaging: resolution, format, experiment ID
* Climate: sensor type, geolocation, timestamp

This enables **discipline-aware recall**, smarter tiering, and scientific auditing.

<!-- 
surgical strike**:

1. Script TSM restores (via its CLI: `dsmc retrieve`, `dsmc restore`)
2. Pipe restored data into **your system’s ingest path** (e.g., Permafrost + Spool)
3. Automate dedup, metadata tagging, and cold migration
4. Slowly cut off TSM by flipping new backups to your system

Low risk, high disruption.

we got an early idea. the architecture should be simple:

[ Aurora ]  ← user client UI (CLI/GTK)
     ↓
[ StubFS ] ← POSIX interface with stubs & triggers
     ↓
[ Permafrost ] ← HSM bot: schedules recall/migration
     ↓
[ Stratum ] ← tiering engine (policy + metadata eval)
     ↓
[ Tundra ] ← cold storage (file/archive manager)
     ↓
[ Spool ] ← tape backend + slot/drive control



who will know what tape drive and what tapes are available?

**Spool** owns that. It manages:

* Tape inventory (barcode, slot, label)
* Drive availability and status
* Mount/unmount operations
* Conflicts, queues, and reservations

Permafrost asks, Spool answers.
Confidence: 99%


-->


