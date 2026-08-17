# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **843.7 ms**
- Average token reduction vs full source context: **8.7%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.2 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G08 | long_term | PASS | 1358.8 | 545 | 0.0% |  |
| G09 | long_term | PASS | 1056.4 | 897 | 0.0% |  |
| G12 | semantic | PASS | 250.9 | 365 | 20.5% |  |
| G14 | semantic | PASS | 243.6 | 217 | 43.9% |  |
| G15 | semantic | PASS | 330.3 | 217 | 52.7% |  |
| G19 | mixed | PASS | 1352.9 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1035.9 | 899 | 0.0% |  |
| G04 | long_term | PASS | 1166.4 | 897 | 0.0% |  |
| G05 | long_term | PASS | 1040.6 | 892 | 0.0% |  |
| G10 | episodic | PASS | 258.2 | 363 | 0.0% |  |
| G11 | episodic | PASS | 247.1 | 454 | 0.0% |  |
| G13 | semantic | PASS | 260.5 | 363 | 35.8% |  |
| G16 | mixed | PASS | 1622.7 | 581 | 0.0% |  |
| G18 | mixed | PASS | 545.3 | 489 | 13.5% |  |
| G20 | mixed | PASS | 1914.9 | 831 | 0.0% |  |
| G06 | long_term | PASS | 1089.8 | 898 | 0.0% |  |
| G07 | long_term | PASS | 1514.6 | 898 | 0.0% |  |
| G17 | mixed | PASS | 1584.5 | 581 | 8.1% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G08 - long_term

`<USER_SUMMARY> Lan's project is LOTUS-88. Lan prioritizes Java and Spring Boot for backend development, and does not use Python. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples. </EPISODES>  <FACT`

### G09 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G12 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal `

### G14 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G15 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> Lan's project is LOTUS-88. Lan prioritizes Java and Spring Boot for backend development, and does not use Python. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples. </EPIS`

### G03 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G04 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G05 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G10 - episodic

`EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. metadata= EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. metadata= EPISODE: Minh dang lam kiem ke lai mo hinh cac du an backend de bao cao, ma minh rat so cai vu bi gan nham du an cua nguoi khac vao ho so cua minh, chuyen do tung xay ra roi nen lan nay minh can cham. Ban liet ke gium minh chinh xac nhung du an backend ma dich than minh dang so huu tho`

### G11 - episodic

`EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. metadata= EPISODE: Minh dang lam kiem ke lai mo hinh cac du an backend de bao cao, ma minh rat so cai vu bi gan nham du an cua nguoi khac vao ho so cua minh, chuyen do tung xay ra roi nen lan nay minh can cham. Ban liet ke gium minh chinh xac nhung du an backend ma dich than minh dang so huu thoi nhe, tuyet doi dung suy dien hay them vao bat ky du an nao cua ban be, dong nghiep hay ai khac `

### G13 - semantic

`EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data witho`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as A`

### G18 - mixed

`<EPISODIC> EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. metadata= EPISODE: Minh dang lam kiem ke lai mo hinh cac du an backend de bao cao, ma minh rat so cai vu bi gan nham du an cua nguoi khac vao ho so cua minh, chuyen do tung xay ra roi nen lan nay minh can cham. Ban liet ke gium minh chinh xac nhung du an backend ma dich than minh dang so huu thoi nhe, tuyet doi dung suy dien hay them vao bat ky du an nao cua ban be, dong nghiep h`

### G20 - mixed

`<LONG_TERM> <USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as A`

### G06 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G07 - long_term

`<USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as ASYNC-FIX-20.`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS. Minh prefers Python for personal demos like ORCHID-27. The user's personal project is named ORCHID-27. The user needs to complete a benchmark report by Friday at 16:00, which is an open loop LAB-REPORT-1600. The user is currently debugging async HTTP and attempted to increase the timeout to 60 seconds, but it still failed. The user asked to check the connection pool, client lifecycle, and concurrency. The effective solution was to reuse the aiohttp ClientSession and set concurrency to 20. The main issue was connection churn, not the timeout threshold. This incident is referred to as A`
