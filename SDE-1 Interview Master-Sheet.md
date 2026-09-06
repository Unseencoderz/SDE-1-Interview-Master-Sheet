### Prep target: Amazon · Microsoft · Tower Research · PhonePe · Zomato-style Tier-1 loops (2026 campus cycle)

> **How this sheet is organized:** five rounds, in the order most Tier-1 companies actually run them. Work top to bottom. DSA and CS-fundamentals sections are intentionally terse (titles + one-liners + links) so you spend your time *solving and reading*, not reading me.

---

## Company Cheat-Sheet: Where Each Round Gets Heavy

Based on 2025–26 interview reports, here's where each company loads the bar. Calibrate your prep time accordingly.

| Company | OA | DSA depth | LLD / Machine Coding | HLD | Behavioral weight |
|---|---|---|---|---|---|
| **Amazon** | 2 coding Qs + work-style/aptitude section | Medium–Hard, standard patterns | Light at SDE-1 (parking lot / vending machine level) | Light — "designing a URL shortener" level, not distributed-systems depth | **Very heavy.** Every interviewer scores you against 2–3 Leadership Principles; the **Bar Raiser round is a hard veto** — you can ace every LP interview and lose the loop here. |
| **Microsoft** | Codility, 3 coding Qs (90 min) | Medium–Hard, tree/graph/DP heavy, plus STL/language internals | Sometimes (LRU cache, parking lot with SOLID) | **Not typically evaluated at SDE-1 (L59/60)** — focus stays on coding | The final **"As Appropriate" (AA) round** is a mixed technical+behavioral gate run by a senior engineer/manager and carries real veto power. Growth-mindset framing matters. |
| **PhonePe** | OA (DSA + MCQ) | 1–2 hard problems per round | **Heavy.** Machine coding round (60–120 min) explicitly tests SOLID, design patterns, class design | Present even at junior levels — HLD round is common | HM (Hiring Manager) round, moderate weight |
| **Zomato** | 3 DSA (medium–hard) + 16–18 MCQs, 90 min | Heavy — 2 technical rounds, each with 1–2 DSA problems | Sometimes, folded into project/HLD discussion | Asked for stronger candidates | "Culture fit" round — genuine, not just a formality |
| **Tower Research Capital** | HackerRank: MCQs (CS fundamentals) + 1–2 coding + a **debugging** section (fix broken C++ code) | Heavy — LC-medium style, but interviewers push variants live and probe STL internals | Rare | Not typical for SDE-1 | Present but lighter — expect probability/math and CS-fundamentals questions blended into "technical" rounds, on top of pure coding |

---

## ROUND 1 — DSA (Online Assessment + Coding Rounds)

**Format:** Titles only (LeetCode # where applicable, GfG for problems without an LC equivalent) + one line on *why interviewers keep reaching for this specific problem*. Do not just memorize solutions — know the pattern well enough to solve an unseen variant, since Tier-1 interviewers (Tower especially) explicitly pivot to variants once you solve the base problem.

### Arrays & Strings
- **Two Sum (LC 1)** — the universal warm-up; tests whether hashmap-for-O(n) is your reflex, not your last resort.
- **Maximum Subarray / Kadane's Algorithm (LC 53)** — cleanest test of whether you can reason about a DP recurrence without calling it "DP."
- **Product of Array Except Self (LC 238)** — forces a no-division, O(1)-extra-space constraint; separates people who understand prefix/suffix products from people who don't.
- **3Sum (LC 15)** — sorting + two-pointer + duplicate handling in one problem; a classic filter for careful edge-case coding.
- **Merge Intervals (LC 56)** — interval problems appear constantly in scheduling/booking-style follow-ups (calendar, meeting rooms).
- **Trapping Rain Water (LC 42)** — a favorite "hard" filter; three valid approaches (brute, prefix-max, two-pointer) let the interviewer watch you optimize live.

### Two Pointers & Sliding Window
- **Longest Substring Without Repeating Characters (LC 3)** — the sliding-window template question almost everyone gets asked in some form.
- **Minimum Window Substring (LC 76)** — the hardest common variant of the window-shrink pattern; tests whether you truly understand window invariants or memorized the easy version.
- **Longest Repeating Character Replacement (LC 424)** — window + frequency-count combo, popular because it looks like LC 3 but needs a different invariant.
- **Container With Most Water (LC 11)** — a clean greedy-two-pointer proof question; interviewers like asking you to *prove* why moving the shorter pointer is correct.
- **Sliding Window Maximum (LC 239)** — the standard monotonic-deque question; separates candidates who know deque-based windows from those who only know two-pointer windows.

### Binary Search
- **Search in Rotated Sorted Array (LC 33)** — tests whether you can adapt binary search invariants instead of just applying the standard template.
- **Find Minimum in Rotated Sorted Array (LC 153)** — a common LC-33 follow-up asked back-to-back.
- **Median of Two Sorted Arrays (LC 4)** — a go-to "hard" filter at Microsoft/Amazon; tests binary-search-on-answer thinking, not array-merging.
- **Koko Eating Bananas (LC 875)** — the canonical "binary search on the answer" problem; if you can recognize this pattern you can solve half the "minimize the maximum" family.
- **Aggressive Cows (GfG)** — the sibling pattern to Koko, "maximize the minimum"; commonly paired in the same round to check pattern transfer, not memorization.

### Linked List
- **Reverse Linked List (LC 206)** — trivial to state, but interviewers watch pointer-juggling discipline closely; iterative *and* recursive versions are usually both asked.
- **Linked List Cycle II (LC 142)** — Floyd's cycle detection plus finding the cycle start; a favorite because the "why does the math work" follow-up filters memorizers.
- **Merge K Sorted Lists (LC 23)** — heap + linked-list combo; a very common "hard" bar-raising question at Amazon/Microsoft.
- **Copy List with Random Pointer (LC 138)** — tests hashmap-based cloning vs. the O(1)-space interleaving trick; a strong space-complexity filter.
- **Add Two Numbers (LC 2)** — deceptively simple carry-handling problem, popular as a fast warm-up before a harder second question.

### Stacks & Queues
- **Valid Parentheses (LC 20)** — the fastest possible stack-fluency check, usually the opener in an OA.
- **Daily Temperatures (LC 739)** — the standard monotonic-stack introduction problem.
- **Largest Rectangle in Histogram (LC 84)** — the hardest common monotonic-stack question; a strong signal problem at Amazon/Microsoft onsite rounds.
- **Min Stack (LC 155)** — an "auxiliary data structure design" question that tests O(1) amortized thinking under a twist.
- **LRU Cache (LC 146)** — appears in *both* the DSA round and the LLD round; doubly linked list + hashmap combo is asked so often it's non-negotiable.

### Recursion & Backtracking
- **Subsets (LC 78)** — the cleanest intro to the "include/exclude" recursion tree that underlies most backtracking.
- **Permutations (LC 46)** — tests in-place swapping vs. visited-array approaches; a common follow-up asks you to handle duplicates (LC 47).
- **Combination Sum (LC 39)** — unbounded-choice backtracking with pruning; a good test of whether you prune *before* recursing.
- **N-Queens (LC 51)** — the classic constraint-satisfaction backtracking problem; asked to check whether you can design pruning conditions from scratch.
- **Word Search (LC 79)** — grid backtracking with visited-state management; a frequent "medium" filter across all five companies.

### Trees — heavy emphasis
- **Maximum Depth of Binary Tree (LC 104)** — the fastest possible tree-recursion fluency check.
- **Validate Binary Search Tree (LC 98)** — tests whether you understand BST invariants globally (min/max bound passing) vs. only locally.
- **Lowest Common Ancestor of a Binary Tree (LC 236)** — one of the single most-repeated tree questions across every company on this list; the "no-parent-pointer, general binary tree" version is the one that actually gets asked.
- **Binary Tree Level Order Traversal (LC 102)** — BFS-on-trees fluency; the base for a dozen "print by level" variants.
- **Serialize and Deserialize Binary Tree (LC 297)** — a strong signal-hard question; tests whether you can design an unambiguous encoding, not just traverse.
- **Diameter of Binary Tree (LC 543)** — the classic "compute a global answer while returning a local value" recursion pattern.
- **Binary Tree Maximum Path Sum (LC 124)** — the hardest common variant of the same pattern as Diameter; a frequent Amazon/Microsoft bar-raiser question.
- **Construct Binary Tree from Preorder and Inorder Traversal (LC 105)** — tests whether you understand traversal orderings deeply enough to reverse-engineer structure.
- **Kth Smallest Element in a BST (LC 230)** — in-order traversal + early termination; a good "did you actually use the BST property" filter.
- **Vertical Order Traversal of a Binary Tree (LC 987)** — a favorite Amazon question; combines BFS/DFS with careful tie-breaking logic.

### Graphs — heavy emphasis
- **Number of Islands (LC 200)** — the single most-repeated "convert a grid to a graph" problem across every company; the baseline BFS/DFS fluency check.
- **Clone Graph (LC 133)** — hashmap + graph-traversal combo; tests visited-state handling on graphs (not just trees).
- **Course Schedule (LC 207)** and **Course Schedule II (LC 210)** — topological sort via both DFS-cycle-detection and Kahn's algorithm; a near-universal "does the candidate know topo sort" filter.
- **Rotting Oranges (LC 994)** — multi-source BFS; a favorite because it looks like a simple grid problem but the "multi-source" twist trips up people who only know single-source BFS.
- **Pacific Atlantic Water Flow (LC 417)** — reverse-thinking-on-a-graph problem (flow backward from the boundary); tests whether you can flip a problem's framing.
- **Network Delay Time (LC 743)** — the standard "implement Dijkstra from scratch" question, very common at Amazon and Tower Research given their systems/latency framing.
- **Cheapest Flights Within K Stops (LC 787)** — a Dijkstra/Bellman-Ford variant with a stop-count constraint; tests whether you understand *why* vanilla Dijkstra breaks here.
- **Number of Connected Components / Redundant Connection (LC 323 / LC 684)** — the standard Union-Find (Disjoint Set) introduction pair; DSU comes up constantly in graph and "connectivity" system-design follow-ups.
- **Alien Dictionary (LC 269, premium but widely asked via GfG equivalent)** — topological sort applied to a non-obvious graph construction; a strong "can you model the problem as a graph at all" filter.
- **Is Graph Bipartite? (LC 785)** — 2-coloring via BFS/DFS; commonly paired with cycle-detection questions.

### Dynamic Programming — heavy emphasis
- **Climbing Stairs (LC 70)** — the "hello world" of DP; mainly used to check you can identify state and transition without overthinking.
- **House Robber (LC 198)** and **House Robber II (LC 213)** — the standard 1D-DP-with-a-constraint introduction; the circular-array twist in part II is the actual filter.
- **Coin Change (LC 322)** — unbounded knapsack; a near-universal DP question because it has a clean state definition but a non-obvious "why does this work" proof.
- **Longest Increasing Subsequence (LC 300)** — asked for the O(n²) DP *and* the O(n log n) patience-sorting/binary-search optimization; the follow-up separates strong candidates.
- **Longest Common Subsequence (LC 1143)** — the base 2D string-DP pattern that underlies Edit Distance, Diff tools, and dozens of variants.
- **Edit Distance (LC 72)** — the canonical "hard" 2D DP; a frequent Amazon/Microsoft/PhonePe bar-raiser because the transition has three cases to get right.
- **0/1 Knapsack (GfG)** — not on LeetCode directly but the conceptual root of Partition Equal Subset Sum, Target Sum, and half the "can you pick a subset" DP questions.
- **Partition Equal Subset Sum (LC 416)** — knapsack applied to a "does a subset exist" framing; a common way to test if you can transform a problem into a known template.
- **Word Break (LC 139)** — string DP with a dictionary lookup twist; tests whether you memoize on index rather than re-deriving substrings.
- **Unique Paths / Minimum Path Sum (LC 62 / LC 64)** — grid DP fluency; usually asked as a fast opener before a harder DP question in the same round.
- **Longest Palindromic Substring (LC 5)** — DP, expand-around-center, and Manacher's are all valid; interviewers use the follow-up ("can you do better than O(n²)?") to gauge depth.
- **Burst Balloons (LC 312)** — interval DP at its hardest; shows up specifically at PhonePe/Amazon-style "hard" filters (also reported directly in PhonePe SDE loops).

### Greedy
- **Jump Game / Jump Game II (LC 55 / LC 45)** — tests whether you can prove a greedy choice is optimal, not just code it.
- **Gas Station (LC 134)** — a favorite because the O(n) greedy insight (total sum ≥ 0 guarantees a solution exists) is genuinely non-obvious.
- **Task Scheduler (LC 621)** — greedy + math (idle-slot counting) combined; also solvable with a heap, so interviewers use it to see which approach you reach for first.
- **Non-overlapping Intervals (LC 435)** — interval-greedy sibling of Merge Intervals; tests sorting-by-the-right-key intuition.
- **Partition Labels (LC 763)** — a clean, fast greedy question often used as a confidence-building second question in a round.

### Heaps / Priority Queue
- **Kth Largest Element in an Array (LC 215)** — tests heap vs. quickselect trade-off reasoning (average O(n) vs O(n log k)).
- **Top K Frequent Elements (LC 347)** — hashmap + heap (or bucket sort) combo; a very common "combine two data structures" filter.
- **Find Median from Data Stream (LC 295)** — the classic two-heap design question; a strong signal for "can you design a data structure," not just use one.
- **K Closest Points to Origin (LC 973)** — heap vs. quickselect again, in a geometry wrapper; common as a fast Amazon OA question.

### Trie
- **Implement Trie / Prefix Tree (LC 208)** — the base data structure question; expect a live implementation, not just usage.
- **Word Search II (LC 212)** — Trie + backtracking-on-a-grid combined; a strong "hard" filter that tests whether you can combine two structures under time pressure.
- **Design Add and Search Words Data Structure (LC 211)** — Trie with wildcard search; tests recursive traversal over a Trie.

### Bit Manipulation
- **Single Number (LC 136)** — the canonical XOR-trick question; fast, but the follow-ups (Single Number II/III) test whether you actually understand XOR properties.
- **Number of 1 Bits (LC 191)** — Brian Kernighan's algorithm; a common "know the O(set bits) trick" check.
- **Counting Bits (LC 338)** — DP + bit manipulation combined; tests if you can find the `i & (i-1)` recurrence.
- **Sum of Two Integers (LC 371)** — add without `+`/`-`; a pure bit-manipulation stress test, occasionally used at Tower Research given their low-level/debugging emphasis.

### "Design a Data Structure" (crosses DSA and LLD)
- **LRU Cache (LC 146)** — doubly linked list + hashmap; the single most cross-company-repeated design question on this entire sheet.
- **LFU Cache (LC 460)** — the harder sibling of LRU; a strong signal-hard question when interviewers want to push further.
- **Insert Delete GetRandom O(1) (LC 380)** — array + hashmap combo for O(1) everything; tests creative data-structure combination.
- **Design Twitter (LC 355)** — heap + hashmap + graph-like follow relationships; a favorite because it's a mini system-design question disguised as DSA.

---

## ROUND 2 — Machine Coding / OOP

### OOP Fundamentals — question list (no long answers here; go deep at the link)
- What are the four pillars of OOP, and how does each show up in a real codebase, not just in theory?
- Abstraction vs. Encapsulation — where do people conflate these, and what's the actual distinction?
- Function overloading vs. overriding — compile-time vs. runtime resolution.
- Interfaces vs. abstract classes — when would you choose one over the other?
- What is the diamond problem, and how do different languages resolve (or avoid) it?
- Deep copy vs. shallow copy — what breaks if you get this wrong in a copy constructor?
- Association vs. Aggregation vs. Composition — the "has-a" relationship spectrum, and why it matters for LLD.
- Static vs. dynamic (early vs. late) binding.
- What is a virtual function, and how does a vtable work under the hood?
- Composition over inheritance — why is this a widely repeated design principle, and when does it break down?

**Resource:** https://www.geeksforgeeks.org/interview-prep/object-oriented-programming-oop-tutorial/ and https://www.geeksforgeeks.org/object-oriented-programming-oop-tutorial/

### SOLID Principles — question list
- Explain each SOLID letter with one real violation you've seen or written yourself.
- Single Responsibility — how do you spot a class that's silently doing two jobs?
- Open/Closed — how does the Strategy pattern help you satisfy this in practice?
- Liskov Substitution — the classic Square-extends-Rectangle counterexample.
- Interface Segregation vs. Single Responsibility — how are these different?
- Dependency Inversion — how does this relate to dependency injection?

**Resource:** https://www.geeksforgeeks.org/system-design/solid-principle-in-programming-understand-with-real-life-examples/

### Design Patterns most likely to be asked
- **Singleton** — thread-safety pitfalls (double-checked locking, eager vs. lazy init) are the actual interview question, not the pattern itself.
- **Factory / Abstract Factory** — used constantly as the "how would you instantiate different payment methods / notification channels" follow-up.
- **Observer** — the backbone of every "design a notification system" or "design a pub-sub" machine-coding question.
- **Strategy** — the go-to answer for "how do you make an eviction policy / discount rule pluggable" (directly relevant to your LRU-style cache work).
- **Decorator** — asked when interviewers want to test composition-over-inheritance in a concrete scenario (e.g., "add toppings to a pizza" or "wrap a data stream").
- **Builder** — asked whenever an object has many optional constructor parameters.

**Resource:** https://www.geeksforgeeks.org/system-design/software-design-patterns/

### Machine Coding / LLD Problems (design + code, usually 60–120 min)
- **Design a Parking Lot** — the single most repeated LLD problem industry-wide; tests class hierarchy design (vehicle types, spot types) and a clean allocation strategy.
- **Design an Elevator System** — state-machine thinking (idle/moving/door-open) plus request-scheduling logic (SCAN-like algorithms).
- **Design a Rate Limiter** — directly relevant to your resume; interviewers ask you to implement token-bucket or sliding-window-counter logic in-memory, then ask how you'd make it distributed (this is where your Redis `INCR`+`EXPIRE` experience becomes a real asset — be ready to explain it unprompted).
- **Design Splitwise / an Expense-Sharing App** — tests graph-like debt-simplification logic plus clean OOP for users/groups/expenses.
- **Design an LRU/LFU Cache (from scratch, in a class)** — the LLD version of the DSA question above; now graded on class design and encapsulation, not just algorithmic correctness.
- **Design a Vending Machine / Tic-Tac-Toe / Snake and Ladder** — state-machine-driven design problems used to check whether you default to clean enums/interfaces over a pile of if-else.
- **Design a Logging Framework** — tests Singleton + Strategy (different log levels/sinks) in combination.
- **Design a Notification System (Email/SMS/Push)** — Observer + Factory combo; a natural extension of your URL-shortener project's service-boundary thinking.
- **Design BookMyShow / a Movie Ticket Booking System** — concurrency-aware LLD; tests how you prevent double-booking of the same seat (this maps directly to your row-lock fallback design in the URL shortener).

**Resource for structured LLD practice:** https://github.com/ashishps1/awesome-low-level-design

---

## ROUND 3 — CS Fundamentals (OS / DBMS / Computer Networks)

**Format:** question list only — go deep at the linked resource, don't try to memorize an essay-length answer here.

### Operating Systems
- What's the difference between a process and a thread, and why is context-switching cheaper for threads?
- What are the four necessary conditions for deadlock, and how does the Banker's Algorithm avoid it?
- Explain paging vs. segmentation, and what problem each solves.
- What is virtual memory, and how does a page fault get handled end to end?
- Compare page replacement algorithms: FIFO, LRU, Optimal — and explain Belady's Anomaly.
- Mutex vs. Semaphore — what's the actual mechanical difference, not just "one is binary"?
- What is a race condition, and how do you prevent one with synchronization primitives?
- Explain the producer-consumer problem and how a bounded buffer solves it.
- What is thrashing, and what causes it?
- Explain the difference between preemptive and non-preemptive scheduling, with one algorithm each.

**Resource:** https://www.geeksforgeeks.org/operating-systems/operating-systems/ · Deadlock deep-dive: https://www.geeksforgeeks.org/operating-systems/introduction-of-deadlock-in-operating-system/ · Interview-question compilation: https://www.geeksforgeeks.org/operating-systems/operating-systems-interview-questions/

### DBMS
- Explain the ACID properties with one concrete example of what breaks if each is violated.
- What are the normal forms (1NF–BCNF), and why does over-normalizing hurt performance?
- Clustered vs. non-clustered index — what's actually different about how the data is stored?
- Explain the different types of SQL joins (inner, left, right, full, self) with a one-line use case each.
- What is a deadlock in a database, and how does it differ from an OS deadlock?
- Explain isolation levels (Read Uncommitted → Serializable) and what anomaly each one prevents.
- What's the difference between a primary key, a unique key, and a foreign key?
- B-Tree vs. B+ Tree — why do databases prefer B+ Trees for indexing?
- What is a transaction, and how do the different types of schedules (serial, serializable, conflict-serializable) relate to it?
- SQL vs. NoSQL — when would you actually choose one over the other for a system you're designing? (This connects directly to your PostgreSQL + Redis combination in the URL shortener — be ready to justify that choice.)

**Resource:** https://www.geeksforgeeks.org/dbms/dbms/ · ACID: https://www.geeksforgeeks.org/dbms/acid-properties-in-dbms/ · Normalization: https://www.geeksforgeeks.org/dbms/introduction-of-database-normalization/ · Indexing: https://www.geeksforgeeks.org/dbms/indexing-in-databases-set-1/

### Computer Networks
- Explain the OSI model layer by layer, and map each layer to a real protocol.
- Walk through the TCP 3-way handshake and the 4-way termination.
- TCP vs. UDP — trade-offs, and one real system that should use each.
- What happens, end to end, when you type a URL into a browser and hit Enter?
- Explain DNS resolution, and what a CDN does to speed it up.
- What is the difference between HTTP and HTTPS, and how does TLS handshake work at a high level?
- Explain congestion control (slow start, congestion avoidance) at a conceptual level.
- What's the difference between a router, a switch, and a hub?
- What is NAT, and why do we need it?
- Explain the difference between a forward proxy and a reverse proxy — and where a rate limiter/API gateway (like the one in your project) typically sits.

**Resource:** https://www.geeksforgeeks.org/computer-networks/computer-network-tutorials/ · TCP handshake: https://www.geeksforgeeks.org/computer-networks/tcp-3-way-handshake-process/ · OSI model: https://www.geeksforgeeks.org/computer-networks/layers-of-osi-model/

---

## ROUND 4 — System Design & Project Deep-Dive

### SDE-1-Level HLD Warm-ups (structured thinking > distributed-systems depth)
- **Design a URL Shortener** — the single most common junior HLD prompt industry-wide; you should be able to answer this in your sleep given your project.
- **Design a Parking Lot at Scale** — HLD version of the LLD problem: now add multiple locations, a central booking service, and payment integration.
- **Design a Rate Limiter as a Standalone Service** — token bucket vs. sliding-window-counter vs. leaky bucket, and how to make it correct across multiple replicas (this is precisely what your resume already claims — be the strongest person in the room on this one).
- **Design a Notification/Alerting System** — fan-out patterns, retry/backoff, and idempotency.
- **Design a Basic Twitter Feed / News Feed at Small Scale** — push vs. pull model for feed generation, and why hybrid approaches exist.
- **Design a Vending Machine / Splitwise at System Scale** — tests whether you can zoom out from LLD to services, queues, and datastores.

### Deep-Dive: Your Project 2 — "URL Shortener with Microservice Architecture"

This is the project most likely to get torn apart, because it's rich in explicit architectural claims. Expect every claim on your resume to be interrogated individually. Prepare tight, specific answers — vague answers here read as resume padding, and interviewers notice immediately.

**Architecture & service boundaries**
- Why five separate microservices instead of a modular monolith? At what team size or traffic level does that decomposition actually start paying for itself, and did your system operate anywhere near that scale?
- Walk me through what happens, service by service, from the moment a `POST /shorten` request hits your API Gateway to the moment a row is committed in Postgres.
- How do your services discover and communicate with each other — direct HTTP calls, a service mesh, or something else? What happens if the auth service is temporarily unreachable when the shortening service needs to validate a token?
- If you had to merge this back into a single deployable service tomorrow, what would you lose, and what would you gain?

**API Gateway & rate limiting**
- You used a Redis `INCR` + `EXPIRE` fixed-window counter for rate limiting. What's the classic weakness of fixed-window counting at window boundaries, and why didn't you use a sliding-window or token-bucket approach instead?
- You claim this stays correct "across multiple gateway replicas" — what specifically makes it correct? What would break if two gateway replicas both call `INCR` at the exact same millisecond without you having thought about atomicity?
- What happens to your rate limiter if the Redis instance backing it goes down? Does your API Gateway fail open or fail closed, and which did you choose, and why?

**Redis cache-aside pattern**
- Why cache-aside instead of write-through or write-behind for redirect lookups? What would you have had to change about your write path to support write-through instead?
- You chose a 1-hour TTL — walk me through the actual trade-off calculation you made between staleness and DB load. What would you change if a URL's destination could be updated by its owner?
- What happens on a cache miss under high concurrent load — could you get a thundering-herd problem where 10,000 requests for the same cold key all hit Postgres simultaneously? How would you prevent that?

**Short-code generation**
- Explain exactly how the Base62-encoded Redis `INCR` counter produces a collision-free code. What's the actual mapping from a monotonically increasing integer to your 6-7 character code?
- You mention a "Postgres row-lock fallback" — fallback from what condition, specifically? What has to go wrong with Redis for this fallback path to trigger, and how does your system detect that it should switch over?
- A monotonic counter means your short codes are sequential and guessable/enumerable. Is that a problem for this product, and if so, how would you fix it without reintroducing collision-retry logic?

**Kafka & the analytics pipeline**
- Why Kafka specifically instead of a simpler message queue (RabbitMQ, SQS) for click-tracking? What property of Kafka are you actually relying on here — ordering, replayability, throughput, or something else?
- You claim redirects keep working via "graceful degradation" if Kafka is down — does that mean click events are silently dropped, buffered locally, or something else? What's your actual data-loss guarantee, and are you okay with it for an analytics use case?
- How would a consumer re-processing the same click event twice (at-least-once delivery) affect your analytics numbers, and how would you make the pipeline idempotent if it mattered?

**Data layer & scale**
- What does your Postgres schema actually look like for the URL-mapping table, and what's your indexing strategy on the short code column?
- At what request-per-second number does this whole architecture start to bend, and which single component bends first — the Gateway, Redis, Postgres, or Kafka?
- If you had to add multi-region support tomorrow, what's the single hardest piece of this system to make work correctly across regions, and why?

**General project-defense questions (apply to any project, use for LearnSpace too)**
- What was the single hardest bug you personally debugged in this project, and how did you actually track it down?
- If you rebuilt this today with everything you now know, what's the first architectural decision you'd change?
- What's a metric on this project you can't currently measure but wish you could — and how would you go about instrumenting it?

---

## ROUND 5 — HR / Behavioral (Bar Raiser, AA Round, Hiring Manager, Culture Fit)

**Format:** question + strategic framework only. No scripted answers — a memorized answer is the fastest way to fail a follow-up.

### The core framework: STAR
- **Situation** — set the scene in 1-2 sentences. Don't over-narrate; the interviewer wants to get to the Action fast.
- **Task** — what were *you* specifically responsible for (not your team)?
- **Action** — the majority of your answer lives here. Use "I," not "we." Be specific about the decision you made and why, not just what you did.
- **Result** — quantify it wherever you possibly can ("reduced load time by 40%" beats "made it faster"). If your resume already has a number, reuse it here — your LearnSpace metrics (70% faster resource discovery, 1.2s load time, 500+ daily sessions) are exactly the kind of concrete results to slot in.

### At Amazon specifically: upgrade STAR to STAR+LP
Amazon interviewers are each assigned 2-3 specific Leadership Principles to score you against. Before the interview, map your own stories to specific LPs so you're not improvising the connection live:
- Have 2-3 stories ready that map cleanly to **Ownership**, **Bias for Action**, **Dive Deep**, **Deliver Results**, and **Earn Trust** — these are the most-asked LPs for SDE-1 loops.
- End your Result with an explicit, natural callback to the principle ("that's the moment I really internalized what ownership means on a small team") rather than naming the LP outright, which can feel forced.
- The Bar Raiser round often deliberately probes for *contradictions* between your stories across different interviewers — stay consistent, don't invent a different "hardest challenge" for every round.

### At Microsoft specifically: the AA round tests growth mindset
- Expect a genuine mix of technical and behavioral — this is not a rubber-stamp round.
- Frame failure stories around *what you learned and changed*, not just what went wrong — Microsoft's evaluators are explicitly listening for intellectual humility.

### Question bank
- "Tell me about yourself." — Use a present → past → future arc (what you do now, the path that got you here, why this role/company is the logical next step). Keep it under 90 seconds.
- "Tell me about a time you disagreed with a teammate or senior." — Frame around a specific technical disagreement (you have real material here: coordinating a 4-member web dev team at Gravity Technical Society). Show you argued the merits, not the ego, and describe how it actually resolved.
- "Tell me about a time you failed." — Pick something real and moderately significant, not a fake-humble brag. The Result section should show a genuine behavior change afterward.
- "Tell me about a time you had to learn something completely new under time pressure." — Your Kafka/Redis/microservices project is strong raw material here if you didn't have prior production experience with these tools.
- "Why this company?" — Research one specific, current thing (a product, an engineering blog post, a recent launch) rather than reciting generic values language.
- "Tell me about a time you managed conflicting priorities." — Your dual roles (Web Dev Coordinator + Prayaas Coordinator + coursework) are legitimate material — pick one real moment of triage, not a general description of "juggling multiple things."
- "Describe a time you went above and beyond what was asked." — Look for a moment with a measurable outcome; don't default to effort-based framing ("I worked really hard") — outcome-based framing lands better.
- "Where do you see yourself in 3-5 years?" — Anchor this in technical growth (depth in distributed systems, mentoring, ownership of a larger system) rather than a title/promotion timeline, which reads as less genuine.

---

## Final Prep Checklist
- [ ] Solve every DSA pattern above at least once from scratch — recognize the *pattern name*, not just the problem you've seen before.
- [ ] Be able to draw your URL shortener's architecture on a whiteboard from memory, including every service boundary and datastore.
- [ ] Have 5+ STAR stories mapped to specific themes (ownership, conflict, failure, learning-under-pressure, going above expectations) before your first interview, not during it.
- [ ] For Amazon specifically: pre-map those stories to Leadership Principles.
- [ ] Re-read your own resume the night before every interview — you will be asked to defend every single line, including "1200+ problems" and "Knight Badge (Top 3%)."
