𝗖𝗮𝗰𝗵𝗶𝗻𝗴 𝗶𝘀 𝘁𝗵𝗲 𝗿𝗲𝗮𝘀𝗼𝗻 𝘄𝗵𝘆 𝗺𝗼𝗱𝗲𝗿𝗻 𝗮𝗽𝗽𝘀 𝗳𝗲𝗲𝗹 𝗙𝗔𝗦𝗧.....

Day 5 of my System Design journey was all about:
👉 𝗖𝗮𝗰𝗵𝗶𝗻𝗴 & 𝗢𝗽𝘁𝗶𝗺𝗶𝘇𝗮𝘁𝗶𝗼𝗻

One big realization:
Good systems become fast not by increasing DB power…
but by 𝗮𝘃𝗼𝗶𝗱𝗶𝗻𝗴 𝘂𝗻𝗻𝗲𝗰𝗲𝘀𝘀𝗮𝗿𝘆 𝗱𝗮𝘁𝗮𝗯𝗮𝘀𝗲 𝗰𝗮𝗹𝗹𝘀. 😄



🧠 𝟭. 𝗪𝗵𝘆 𝗖𝗮𝗰𝗵𝗶𝗻𝗴 𝗠𝗮𝘁𝘁𝗲𝗿𝘀

Without caching:
User → App → Database

At massive scale, repeated DB reads can:
❌ Increase latency
❌ Increase DB load
❌ Crash systems

👉 Caching reduces repeated reads and speeds up responses.



⚡ 𝟮. 𝗖𝗮𝗰𝗵𝗶𝗻𝗴 𝗣𝗮𝘁𝘁𝗲𝗿𝗻𝘀 𝗟𝗲𝗮𝗿𝗻𝗲𝗱

🔹 Cache-Aside (Lazy Loading)
→ Most common approach

🔹 Write-Through
→ Write to cache + DB together

🔹 Write-Back
→ Write to cache first, DB later asynchronously



🔥 𝟯. 𝗖𝗮𝗰𝗵𝗲 𝗘𝘃𝗶𝗰𝘁𝗶𝗼𝗻 𝗦𝘁𝗿𝗮𝘁𝗲𝗴𝗶𝗲𝘀

Since memory is limited, old data must be removed intelligently.

Learned:
✔ LRU
✔ LFU
✔ FIFO
✔ Random Eviction



📌 𝟰. 𝗪𝗵𝗲𝗿𝗲 𝗖𝗮𝗰𝗵𝗶𝗻𝗴 𝗶𝘀 𝗨𝘀𝗲𝗱

✔ Instagram feed
✔ Netflix content
✔ E-commerce products
✔ Session storage
✔ Rate limiting

👉 Best for 𝗥𝗲𝗮𝗱-𝗛𝗲𝗮𝘃𝘆 𝗦𝘆𝘀𝘁𝗲𝗺𝘀



🌍 𝟱. 𝗧𝘆𝗽𝗲𝘀 𝗼𝗳 𝗖𝗮𝗰𝗵𝗶𝗻𝗴

🖥️ In-Memory Local Cache
☁️ Distributed Cache (Redis, Memcached)
🌐 CDN / Edge Cache
🗄️ Database-Level Cache
📱 Application-Level Cache
💻 OS-Level Cache



🔴 𝟲. 𝗥𝗲𝗱𝗶𝘀 𝗗𝗲𝗲𝗽 𝗗𝗶𝘃𝗲

Learned why Redis is super fast:

✔ In-memory key-value store
✔ Event loop architecture
✔ No heavy context switching
✔ Highly optimized single-threaded model

Also explored:
👉 Redis Cluster
👉 Hash-slot sharding



⚔️ 𝟳. 𝗥𝗲𝗱𝗶𝘀 𝘃𝘀 𝗖𝗗𝗡
Redis → reduces DB/backend load
CDN → reduces network latency globally

👉 Real systems use BOTH together.



🏗️ 𝟴. 𝗠𝘂𝗹𝘁𝗶-𝗟𝗮𝘆𝗲𝗿 𝗖𝗮𝗰𝗵𝗶𝗻𝗴

Real-world systems use multiple layers:

User
↓
CDN (L0)
↓
App Cache (L1)
↓
Redis (L2)
↓
DB Cache (L3)
↓
Disk



💡 𝗕𝗶𝗴 𝗧𝗮𝗸𝗲𝗮𝘄𝗮𝘆:

Caching is literally everywhere.
Modern backend systems rely heavily on smart caching strategies to scale efficiently. 

Day 5 done ✅
