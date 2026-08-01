#domain/1-0-Networking-Concepts

Maps hostname to IP address for [[IPv4]]
32-bit IP address
Can be a fall back if [[MX]] is not available for Mail

- If A record updated and web server is unreachable, you can use nslookup to check the hostname and then flush dns 

- A record is what gets cached, so DNS cache poisoning attacks target A records