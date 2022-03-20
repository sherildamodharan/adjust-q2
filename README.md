Task 2
# Question
- Imagine a server with the following specs:
- 4 times Intel(R) Xeon(R) CPU E7-4830 v4 @ 2.00GHz
- 64GB of ram
- 2 tb HDD disk space
- 2 x 10Gbit/s nics
- The server is used for SSL offloading and proxies around 25000 requests per second.Please let us know which metrics are interesting to monitor in that specific case and how would you do that? What are the challenges of monitoring this?


# Answer:

Metrics


Metric | Usage |
--- | --- | 
CPU usage | CPU usage is important for mission critical proxy servers  |
Memory | Memory usage metric collects the memory usage on a regular interval |
Disk IOPs | measure DISK IO of the server while performing SSL encryption and decryption |
avgLoad | For first glance monitoring and to understand the performance on a regular basis |
filesystem | To expose filesystem stats |
interface stats | Both in and out interfaces need to be monitored for a proxy server |
netstat | To monitor the open session/closed sessions/icmp in and out |
inbound traffic | to understand inbound rate |
outbound traffic | to understand outbound rate |
open sessions | to view open sessions per sec |
closed sessions | to view closed sessions per sec |
new connections | to view the new connections per sec | 

# challenges & workaround: 
- The number of service monitoring need to be minimalised as the proxy servers can bottleneck due to the excessive monitoring asweel at peak times.
- apart from the traffic monitoring, other service monitoring can be initiated with a longer duration understanding the criticality of the server.

