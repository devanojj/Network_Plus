## 1. How to Read Switch Port Status Output


```
Status and Counters - Port Status

            | Intrusion                          MDI        VLAN
 Port Type  | Alert    Enabled Status Mode       Mode  Ctrl Inf
 ---- ----- + -------- ------- ------ ---------- ---- ---- -----
 1    100/1000T | No   Yes     Up     100FDx     MDIX off  2
 5    100/1000T | No   Yes     Up     100HDx     MDIX off  4
 10   100/1000T | No   No      Down   100FDx     MDI  off  4
```

### Scan order (fastest → answer)

1. **Find the relevant VLAN column value first** if the question names a VLAN, host, or subnet — this narrows 10 ports down to 1-2 immediately.
2. **Check Status** — `Down` means no traffic at all (not a performance complaint — a connectivity complaint). Rule these ports out for "slow" issues.
3. **Compare Mode column across all active ports** — the outlier is usually the answer.
    - `100FDx` = Full Duplex — normal/expected
    - `100HDx` = Half Duplex — **the classic mismatch culprit** if every other port is FDx
4. **Check MDI Mode** — `MDI` vs `MDIX` — auto-crossover; rarely the fault unless explicitly tested
5. **Check Flow Ctrl** — usually uniform (`off` across the board); rarely the odd column
6. **Check Intrusion Alert / Enabled** — port security related, different failure mode (port shuts down, doesn't just slow down)

### Key column meanings

|Column|What it tells you|When it's the answer|
|---|---|---|
|**Status**|Up/Down — physical + protocol link state|Question is "no connectivity" not "slow"|
|**Mode**|Speed + Duplex (e.g. `100FDx`, `1000FDx`, `100HDx`)|Question mentions slow transfer rates, retransmissions, collisions|
|**MDI Mode**|MDI (straight) vs MDIX (crossover) — auto-negotiated on modern switches|Rare; usually not the fault on modern gear|
|**Flow Ctrl**|Pause frame negotiation|Rarely tested as the misconfiguration|
|**VLAN Inf**|VLAN assignment for that port|Question specifies a VLAN — use this to filter ports first|

### Symptom → Cause quick match

|Symptom in question|Likely column/cause|
|---|---|
|"Slow transfer rates," "high latency on one link," "retransmissions"|**Duplex mismatch** (one side FDx, other HDx)|
|"No connectivity," "port won't come up"|**Status: Down**|
|"Wrong devices can see each other" / "user can't reach server"|**VLAN Inf misassignment**|
|"Excessive collisions" (legacy Ethernet framing)|**Duplex mismatch**|
|"Port shut down unexpectedly," "unauthorized device"|**Intrusion Alert / port security**|
