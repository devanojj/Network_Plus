#domain/5-0-Network-Troubleshooting

*   **Latency vs. Jitter:** Latency is the delay in packets reaching their destination. Jitter is the *variation* in that delay. Jitter is a killer for real-time traffic like VoIP and video.
*   **Interface Errors:**
    *   **CRC Errors (Cyclic Redundancy Check):** Packets arrived corrupted. Usually indicates a bad physical cable, faulty NIC, or duplex mismatch.
    *   **Runts:** Packets smaller than the minimum 64 bytes. Often caused by collisions.
    *   **Giants:** Packets larger than the maximum 1518 bytes (unless Jumbo Frames are configured).
    *   **Drops:** The router/switch interface buffer is full due to congestion, so it simply discards incoming packets.
*   **Bottlenecking:** The entire network slows down because one single link or device (the bottleneck) cannot handle the throughput capacity.