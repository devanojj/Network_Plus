
*Recursive*
In a recursive lookup, the client machine puts the entire burden of resolution onto the local DNS server. 
The client makes **one single request**. If the local DNS server doesn't have the answer cached, _that server_ goes out and talks to the Root, TLD, and Authoritative servers on behalf of the client.
The server does all the heavy lifting and returns either the **final IP address** or an explicit error.


*Iterative*
In an **iterative lookup**, the DNS server doesn't go chasing down the answer for the querier. Instead, it answers with the best information it currently possesses. 
If the queried DNS server doesn't know the exact IP, it replies with a **referral** to another DNS server that is closer to the answer The querying device must then take that referral and manually contact the next server itself. This repeats until it hits the authoritative source.
**More work** for the client/querier, **less work** for the responding DNS server.


When a user types a URL into a browser, both lookup types are actually used in tandem to find the final destination:



| Feature         | Recursive Look Up                             | Iterative Look Up                                 |
| --------------- | --------------------------------------------- | ------------------------------------------------- |
| Client Workload | Low                                           | High                                              |
| Server Workload | High                                          | Low                                               |
| Use Case        | End-user devices talking to local DNS servers | Local DNS servers talking to Root/TLD servers     |
| Response Type   | The final IP address or a failure message     | Best known answer or a referral to another server |

