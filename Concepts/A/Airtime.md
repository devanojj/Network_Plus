- Wi-Fi is shared time on the air (“airtime”), not shared bandwidth like a cable.
- **Airtime fairness (ATF)**  tries to prevent slow/weak clients from hogging airtime. Every device gets the exact same amount of time (e.g., 10 milliseconds) to talk, regardless of its speed.
- Wi-Fi is half duplex

**Exam scenario:** “One far-away client slows everyone down” → airtime fairness helps mitigate.

Modern features like [[OFDMA]] and [[MU-MIMO]] directly address airtime limits by letting the AP talk to multiple devices at the exact same time.

To preserve airtime for critical corporate traffic, network administrators will often isolate legacy or slow IoT devices onto their own dedicated 2.4 GHz SSID or separate channel entirely, ensuring they don't consume the premium airtime on high-performance 5 GHz or 6 GHz channels.