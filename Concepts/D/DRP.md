**Disaster Recovery Procedure** 

==**BCP vs. DRP**== 
Business Continuity Procedure focuses on keeping the business operational during a crisis. DRP is the technical IT subset of the BCP, focused on restoring IT systems.

**==Metric==**
- RPO (Recovery Point Objective) - How much data loss is acceptable? (Dictates backup frequency)
- RTO (Recovery Time Objective) - How much downtime is acceptable? (Dictates the recovery strategy).
- MTBF (Mean Time Between Failures) - Expected lifetime of a product before it fails (reliability metric).
- MTTR (Mean Time to Repair) - Average time taken to fix a failed system.

**==Recovery Sites:**==
- Cold Site - Empty building with power and cooling, but no hardware or data. Takes weeks to activate.
- Warm Site - Has hardware ready, but data must be restored from backups. Takes days to activate.
- Hot Site - Exact replica of the primary site with live, synchronized data. Takes minutes/hours to activate.