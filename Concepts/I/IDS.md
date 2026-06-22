**Intrusive detection system**


Anomaly IDS / [[Firewall]] is most likely to generate false positives
Establishing a **performance baseline** of what "normal" network behaviour looks like. Anything that deviates from this baseline is flagged as a threat.


Signature-Based: Looks for specific, pre-defined patterns (like a fingerprint or a specific string of malicious code). If the signature matches, it flags it. It rarely generates false positives because the rule is explicit: If it looks exactly like X, block it.


Network-Based (Standard Layer 3/4 Firewalls): These rely on rigid, deterministic Access Control Lists (ACLs) checking source IPs, destination IPs, and ports. A packet is either permitted or denied based on strict rules.


Host-Based: Monitors a single device from the inside. It has deep context regarding exactly which local application or process is generating traffic.


