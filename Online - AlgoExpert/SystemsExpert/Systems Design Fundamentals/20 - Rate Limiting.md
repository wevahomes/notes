# 20 - Rate Limiting

- !!! BRIEF NOTES !!!

- Ramifications:
    - Security.
    - Performance.
- Threshold on certain operations..
- Beyond which, errors are returned.
- Server doesn't contact database, just returns an error.
- Risk:
    - System may come down.
    - Denial of service (DoS) attack.
- Can rate limit based on:
    - User. From header.
    - IP.
    - Region.
- Is not the ultimate way to protect your system.
- More complicated attack:
    - Distributed DOS (DDoS).
- [Coding example].
- Storing our accesses in memory..
- In a distributed system, this could be a problem.
    - Unless you have really configured the load balancing.
- Use a database.
- Can make your rate limiting much more complicated.
- Can have rate limiting tiers.
    - X times in a second.
    - Y times in 10 seconds.
    - Z times in a minutes.
