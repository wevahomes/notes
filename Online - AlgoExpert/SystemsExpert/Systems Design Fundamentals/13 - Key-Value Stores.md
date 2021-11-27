# 13 - Key-Value Stores

- !!! BRIEF NOTES !!!

- Sometimes the structure of a relational DB is cumbersome.
- Popular non-relational DB: Key-Value Store.
- Mappings of keys to values.
- Keys: Typically strings.
- Values: Typically strings.
- Good:
    - Very flexible.
    - Very simple.
- Good for when you don't need that imposed structure.
- Good for cacheing.
- Good for dynamic configuration.
- You access values directly through keys.
    - Faster.
    - Lower latency.
    - Higher throughput.
- Can have in-memory or in-storage key-value stores.
    - In-memory can be good for caching.
- Some will have low consistency and some will have high consistency.
- If you have a local cache, if the server goes down, you can still access the local cache. This might be a good feature.
