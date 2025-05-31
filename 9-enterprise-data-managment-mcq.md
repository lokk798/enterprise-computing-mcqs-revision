# Enterprise Data Management and Caching – MCQs

### 1. What is the **main risk** of using **write-behind caching** in enterprise applications?

- a. Increased latency on write operations
- b. Frequent cache misses
- c. Inconsistent cache due to race conditions
- d. Data loss during cache failure
- e. Poor query performance on large datasets

**Correct Answers:** d  
**Explanation:** Write-behind caching defers writes to the database, improving performance but risking data loss if the cache fails before persistence.

---

### 2. Which of the following scenarios would **least** benefit from cache warming?

- a. Frequently accessed product catalog in an e-commerce app
- b. Weather data that updates every 10 minutes
- c. Static assets served via CDN
- d. On-demand search query results
- e. Product recommendations based on user history

**Correct Answer:** d  
**Explanation:** Cache warming is best for predictable, frequently accessed data. Search results are more ad-hoc and user-specific, reducing cache warm benefits.

---

### 3. In the `@Service` class using Redis, which annotation ensures the class is detected as a Spring-managed component?

- a. @Component
- b. @Service
- c. @Autowired
- d. @EnableCaching
- e. @Configuration

**Correct Answer:** b  
**Explanation:** `@Service` is a specialized stereotype annotation used for service-layer components in Spring.

---

### 4. Which of the following are **valid advantages of using Redis** for caching in enterprise applications?

- a. Low memory usage for large datasets
- b. High throughput read/write operations
- c. Support for a wide variety of data structures
- d. Built-in persistence and replication
- e. Strong consistency guarantees for distributed transactions

**Correct Answers:** b, c, d  
**Explanation:** Redis is fast, supports diverse data types, and provides replication/persistence. It does not provide strong ACID guarantees like traditional databases.

---

### 5. Why is **cache granularity** a crucial decision point in designing caching layers?

- a. It affects key naming conventions
- b. It determines eviction policies
- c. It balances memory use and hit rates
- d. It defines the structure of backend APIs
- e. It determines CDN selection

**Correct Answer:** c  
**Explanation:** Granularity affects the balance between performance and memory footprint. Finer granularity increases hit rate but adds complexity.

---

### 6. What issue might arise if **cache eviction policy** is misaligned with access patterns?

- a. Higher database load
- b. Memory overflow
- c. Increased latency due to stale data
- d. Higher cache hit rate
- e. Lower cache efficiency

**Correct Answers:** a, e  
**Explanation:** A poorly chosen eviction policy may evict frequently needed data, increasing backend access and reducing efficiency.

---

### 7. Which Redis feature is essential for **tracking session data**?

- a. Expiry (TTL) support
- b. Hash data structures
- c. Pub/Sub
- d. Streams
- e. Pipelines

**Correct Answer:** a  
**Explanation:** Session data must expire automatically after inactivity; TTL enables this.

---

### 8. In the Redis CLI, which command retrieves all available keys?

- a. LIST \*
- b. GET \*
- c. KEYS \*
- d. FETCH \*
- e. VALUES \*

**Correct Answer:** c  
**Explanation:** `KEYS *` retrieves all keys, though it’s discouraged in production due to performance.

---

### 9. What is the **primary use** of the `@PostConstruct` annotation in the context of caching?

- a. Invalidating expired cache entries
- b. Setting up cron-based cache cleaning
- c. Initializing the cache with warm data
- d. Configuring Redis cluster nodes
- e. Binding application properties

**Correct Answer:** c  
**Explanation:** `@PostConstruct` initializes the cache with data right after the bean is created.

---

### 10. What risk does **manual cache invalidation** introduce?

- a. Event handling overhead
- b. Risk of race conditions
- c. Tight coupling between layers
- d. Stale data in cache if missed
- e. Automatic data overwrite

**Correct Answer:** d  
**Explanation:** If cache invalidation is missed manually, the cache may serve outdated data.

---

### 11. What is the **most significant benefit** of using **cache tiering**?

- a. Reduced cache complexity
- b. Elimination of backend database
- c. Isolation of cache from application logic
- d. Improved latency and scalability
- e. Avoiding use of compression

**Correct Answer:** d  
**Explanation:** Tiering layers (e.g., in-memory + CDN) allows faster access paths and load distribution.

---

### 12. What does `@EventListener` annotation in Spring Boot accomplish in cache invalidation?

- a. Registers bean for serialization
- b. Subscribes to system health events
- c. Listens to and handles custom published events
- d. Schedules periodic cache refresh
- e. Serializes bean properties for logging

**Correct Answer:** c  
**Explanation:** `@EventListener` listens for application events like custom cache invalidation triggers.

---

### 13. Which of the following are **common cache eviction policies**?

- a. FIFO
- b. TTL
- c. LFU
- d. LRU
- e. RR

**Correct Answers:** a, c, d, e  
**Explanation:** TTL is a time-based invalidation strategy, not an eviction policy. LFU, LRU, FIFO, RR are all eviction strategies.

---

### 14. In a Spring Boot Redis integration, which class provides high-level Redis operations?

- a. RedisRepository
- b. RedisTemplate
- c. RestController
- d. JdbcTemplate
- e. CacheManager

**Correct Answer:** b  
**Explanation:** `RedisTemplate` is Spring’s abstraction for Redis operations.

---

### 15. When is **cache-aside strategy** (lazy loading) most useful?

- a. For write-heavy operations
- b. When caching third-party API results
- c. For frequently updated records
- d. When reads are predictable and repeated
- e. For rarely used metadata

**Correct Answer:** b  
**Explanation:** Cache-aside is great for expensive and infrequent reads, like third-party API responses.

---

### 16. Which tools can help detect frequently accessed data for caching?

- a. ELK Stack
- b. Wireshark
- c. APM tools (e.g., New Relic)
- d. Redis key watchers
- e. Cache miss/hit metrics

**Correct Answers:** a, c, e  
**Explanation:** Tools like ELK, New Relic, and cache hit/miss metrics help analyze access patterns.

---

### 17. Which is a **true statement** about using Redis in Docker?

- a. Redis is not supported in containerized environments
- b. Redis should only be run in root mode
- c. Redis Docker container runs by default on port 3306
- d. Redis must be built from source before running in Docker
- e. Redis can be run with `docker run -p 6379:6379 redis`

**Correct Answer:** e  
**Explanation:** This is the standard command to map Redis's default port when running a container.

---

### 18. Which caching layer offers **protection against DDoS attacks**?

- a. Redis
- b. In-memory caches
- c. CDN
- d. Web server caches
- e. LocalStorage in browsers

**Correct Answer:** c  
**Explanation:** CDNs provide edge-level protection including DDoS mitigation and rate-limiting.

---

### 19. In Spring Security, storing access tokens in Redis helps:

- a. Eliminate CSRF risks
- b. Validate tokens without decoding
- c. Enable stateless authentication
- d. Centralize token revocation
- e. Improve login page rendering

**Correct Answers:** c, d  
**Explanation:** Redis enables quick token lookup and invalidation, ideal for stateless, secure token handling.

---

### 20. What is a **common mistake** when implementing TTL-based cache invalidation?

- a. Setting TTL too short
- b. Using FIFO instead of LFU
- c. Forgetting to configure Redis host
- d. Compressing values before caching
- e. Writing keys with special characters

**Correct Answer:** a  
**Explanation:** Too short a TTL causes frequent cache misses, defeating caching benefits.

---

