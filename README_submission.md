# README Submission — Lab 17

Layer quan trọng nhất trong bộ test này là **long-term memory** vì nó quyết định bốn case E02, E03, E08 và E09: preference qua session, open loop, recency theo scope dự án và user isolation. Context Block của Zep trả về context đã tổng hợp từ user graph, nên giảm công việc tự xây dựng ingestion, graph, provenance và cross-session recall. Đổi lại, nó phụ thuộc dịch vụ cloud và có latency. Redis + Qdrant cho quyền kiểm soát trực tiếp key, TTL, collection và chi phí local, nhưng phải tự làm schema, indexing, retrieval, isolation, conflict handling và lifecycle.

Guardrail chống memory poisoning là chỉ ingest khi có consent và allowlist loại memory; redact PII; lưu source, timestamp, confidence, scope và validity; review mọi preference có tác động cao; không cho heartbeat tự thêm quyền hay instruction mới. Khi conflict, dùng recency kết hợp scope và giữ provenance thay vì xóa lịch sử mù quáng.

Benchmark student đạt 11/11 PASS (100%), nên không có layer yếu nhất: short-term 2/2, long-term 4/4, episodic 2/2, semantic 2/2 và mixed E07 PASS. E02 long-term lấy nhiều token nhất, 897 token. E07 cần ghép long-term `Python` với semantic `Idempotency-Key`. Student giảm context trung bình 19.8% so với full source; no-memory giảm 81.8% nhưng chỉ đạt 2/11 vì gần như không retrieve evidence.

E08 chứng minh recency + scope: BLUEBIRD-42 dùng TypeScript/NestJS nhưng preference Python vẫn đúng cho ORCHID-27. E10 chứng minh compaction giữ durable constraint `REVIEW-DEADLINE-1600`, Friday và 16:00 dù raw turns cũ đã bị evict; buffer không phù hợp vì context tăng tuyến tính.
