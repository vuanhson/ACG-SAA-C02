## Elasticache

ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slower disk-based databases.

ElastiCache supports two open-source in-memory caching engines:
- Memcached
- Redis

Requirement | Memcached | Redis
------------|-----------|------------
Simple Cache to offload DB    | Yes | Yes
Ability to scale horizontally | Yes | Yes
Multi-threaded performance    | Yes | No
Advanced data types           | No  | Yes
Ranking/Sorting data sets     | No  | Yes
Pub/Sub capabilities          | No  | Yes
Persistence                   | No  | Yes
Multi-AZ                      | No  | Yes
Backup & Restore Capabilities | No  | Yes

### Exam Tips
- Use Elasticache to increase database and web application performance.
- Redis is Multi-AZ
- You can do back ups and restores of Redis