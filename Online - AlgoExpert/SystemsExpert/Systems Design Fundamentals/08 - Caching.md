# 08 - Caching

- !!! BRIEF NOTES !!!

- To speed up a system.
- Improve latency.
- Can cache:
    - Network requests.
    - Long computational work.
    - High number of identical requests.
- Can hash a request from a sequence of bytes to an integer and then use a hash map cache.
- Multiple sources of truth.
- Two popular cache mechanisms.
    - Write-through cache.
    - Write-back cache.
        - Async update the database.
- Caches can become stale.
- Can have a single cache (Redis).
- May not care about staleness, eg view count.
- Immutable data - Cache is easy and useful.
- Eviction policies.
    - Least recently used (LRU) policy.
    - Least frequently used (LFU) policy.
    - Last in first out.
