# Hi, I'm Marcelo 👋
 
I build systems at the intersection of **AI agents**, **cryptography**, and **confidential computing**.
 
My background spans cryptographic hardware (PhD), SGX-based key management in production (Ava Labs, $2B+ in assets), and agentic AI systems built with LangGraph, CrewAI, and the Anthropic and OpenAI SDKs.
 
---
 
## Featured Project
 
### 🔒 [Confidential AI Agent](https://github.com/mkaihara/confidential-ai-agent)
 
A LangGraph agent that calls Claude from inside an Intel SGX enclave. The API key never touches the host. Every response is cryptographically signed and independently verifiable via DCAP remote attestation.
 
```
Host (LangGraph) ──TCP──▶ SGX Enclave (Gramine + Python)
                               │
                          Sealed storage
                          API key + ECDSA signing key
                          encrypted with hardware key
```
 
**What makes it real, not conceptual:**
- ECDSA-P256 output signing: `sign(SHA256(prompt ‖ result ‖ timestamp ‖ MRENCLAVE))`
- DCAP quote binds signing key to enclave measurement via Intel's PKI
- Standalone verification CLI — validates the full trust chain without a running enclave
- Sealed storage using `_sgx_mrenclave` hardware key — no external wrap key after bootstrap
---
 
## Stack
 
`Intel SGX` · `Gramine` · `LangGraph` · `Anthropic SDK` · `DCAP attestation` · `Python` · `Azure DCsv3`
 
---
 
## Connect
 
[LinkedIn](https://www.linkedin.com/in/mkaihara) · [marcelokaihara.com](https://www.marcelokaihara.com)
