Network Traffic Analysis: Traceroute & TCP Handshake
Technical study of network routing and reliable transport protocols, completed as part of the Jedha Cybersecurity program.

Objectives
Analyze the route discovery process using UDP and ICMP.

Inspect the 3-way handshake process for reliable TCP connections.

Verify DNS resolution for public domains.

Traceroute & Hop Discovery (UDP/ICMP)
I performed a trace to 8.8.8.8 to analyze how the TTL (Time To Live) mechanism identifies intermediate hops.

Technical Observations:
UDP Probing: A total of 27 UDP packets were sent to discover the network path.

Port Strategy: Destination ports started at 33434, incrementing with each request to track individual probes.

ICMP Responses: Intermediate routers (such as 213.248.91.224 and 62.115.136.224) correctly returned ICMP Type 11 (Time Exceeded).

Final Reach: The destination (8.8.8.8) returned an ICMP Type 3 (Port Unreachable), confirming the trace was successful.

TCP Handshake Analysis
I analyzed the connection establishment with neverssl.com (IP: 34.223.124.45) to verify the reliability of the transport layer.

The 3-Way Handshake Process:
SYN: Initial synchronization request with Relative Sequence Number 0.

SYN-ACK: Server response acknowledging the request and synchronizing parameters.

ACK: Final acknowledgment sent by the client to establish the session.

Note: This laboratory was performed as part of the Jedha Cybersecurity course
