# 09 - Proxies

- !!! BRIEF NOTES !!!

- Forward proxy (aka proxy)
- On the client side/team.
- Can hide the identity of the client.
- The client's source IP address can be replaced by the forward proxy.
- Basically how VPNs work.

- Reverse proxy.
- On the server side/team.
- Need to configure DNS to point to the reverse proxy.
- Request goes to the reverse proxy.
- Client thinks it is communicating with the server.
- Really useful.
    - Filter out requests.
    - Logging.
    - Cache things.
    - Load balancer.
    - Can edit the headers.
