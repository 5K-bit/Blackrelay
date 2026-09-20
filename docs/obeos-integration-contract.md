# BlackRelay integration contract v1

Readiness: scaffold. No runtime service is advertised and no event consumption begins automatically. BlackRelay is a workflow dispatcher, not the event transport.

Input: Event Contract v1 envelopes with stable event_id, timestamp, source and payload. A rule names an event type, bounded predicates, an action adapter and an explicit cooldown. Delivery is at least once: rules deduplicate event_id plus rule version before execution.

Output: proposed action requests to Blackfong. A relay rule cannot grant its own permissions. Filesystem/device actions require Blackfong authorization; Earth controls use Earth Control v1 and the active scene ID. Never dispatch raw JavaScript or shell strings from event payloads.

Required readiness gates before runtime integration: schema tests, deduplication, queue backpressure, dry-run trace, authorization denial tests, startup/shutdown ownership and health endpoint. Report scaffold, disabled, ready, degraded or unavailable explicitly.

Earth depends on the existing OBEOS event store/outbox and operates without BlackRelay. This contract does not claim a completed standalone dispatcher product.
