# DA51 × SLR proof-linked publication boundary

Date: 2026-10-17

ZOS owns publish/pull/mirror orchestration for logical artifact revisions. It does not own DA51 semantics, SLR proof obligations/payments, formal certification, or selector meaning.

For proof-linked artifacts ZOS preserves, when present:

```text
artifactId
artifactRevision
shardId
contentDigest
da51Address
formalDemandRef
formalEvidenceRef
statementDigest
```

The first four remain logical/content identity coordinates under the shared artifact contract. The latter four are provenance joins.

Publication order:

```text
logical artifact revision
 -> logical shard IDs
 -> content-digest validation
 -> materialize HF/IPFS/file object refs
 -> record sink acknowledgement
```

Hard boundaries:

```text
publish success != proof
sink acknowledgement != SLR payment
IPFS CID/HF path != semantic identity
DA51 address/status != theorem authority
formalEvidenceRef != publisher authority
mirror success != security/legal conclusion
```

ZOS must preserve logical shard IDs and provenance fields across mirrors and may never rewrite the formal statement/demand identity to match a sink-specific representation.
