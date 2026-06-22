A loopback test is used to test whether a network interface is working correctly

**Software Loopback**
- The IP address **127.0.0.1** is the loopback address (also called localhost)
- If it responds, your network stack is working correctly
- It never actually sends traffic onto the network — it stays inside the device


**Hardware Loopback**
- A physical **loopback plug** inserted into a port
- Redirects the outgoing signal straight back into the incoming port
- Used to test whether the physical interface/port itself is working
- Useful when you suspect a faulty NIC or port