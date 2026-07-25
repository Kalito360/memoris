# sdk

Client libraries for interacting with Memoris.

Planned interface (Python and TypeScript, matching functionality):

\`\`\`
client.store(agent_id, memory)   # normalize + write memory via the Memoris backend
client.retrieve(memory_id)       # fetch a memory object + its receipt
client.verify(receipt)           # verify a Memoris receipt against Shelby's proof
\`\`\`

Designed to feel like "Shelby, but agent-memory-flavored" — not a competing SDK philosophy, just the right shape for agent developers.

**Status:** not yet implemented — architecture in progress.
