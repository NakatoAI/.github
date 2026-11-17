<p align="center">
  <a href="https://nakato.ai"><img src="https://raw.githubusercontent.com/NakatoAI/.github/main/profile/nakato-logo.png" alt="Nakato logo" width="96"></a>
</p>

## Your AI never meets your customer. It meets their twin.

Nakato is the privacy layer between a regulated organisation's sensitive data and the AI models it wants to use.

Before a request leaves your environment, Nakato finds the personal data (names, account numbers, diagnoses, and the indirect clues that could point to someone) and swaps each value for a **semantic twin**: a fictional stand-in that keeps the context the task needs. The model only sees the twins. When the answer comes back, the originals are restored, still inside your environment. Nakato runs in your own cloud account or on your own servers.

We call this **Reversible Semantic Pseudonymisation (RSP)**.

### How it works

| Step | What happens |
|---|---|
| **Semantic** | Detects direct and indirect identifiers across 50+ entity types and works out what each one means in context |
| **Pseudonymisation** | Replaces each identifier with a semantic twin, so the model keeps the meaning without seeing the person |
| **Reversible** | Logs every substitution locally and restores the originals in the answer |

**What stays with you:** the raw record, the twin-to-original map and the audit trail.
**What reaches the model:** the twin and the task.

- Runs in your VPC or on-premises, including air-gapped setups
- Works with any LLM API
- Handles text, voice recordings and images
- Fails closed: anything below the 95% confidence gate is held back, not passed through

### The evidence

On 500,000 internal financial-services test cases (self-reported), summaries kept 96.2% accuracy after pseudonymisation and reversal, every substitution was reversed, and the layer added 45 to 90ms of latency. Results vary with the kind of document and how Nakato is configured. See the methodology and comparisons at [nakato.ai/benchmarks](https://nakato.ai/benchmarks).

### Is it right for you?

Nakato is built for banks, healthcare, legal and HR teams that need full records to get real value from AI. It is probably not the right fit if you:

- are a technology company with the capacity to build this layer in-house
- need a fully cloud-hosted service (we don't currently offer one)
- need true anonymisation; this is pseudonymisation, and some re-identification risk remains

### For developers

The **RSP SDK** is in early access. Three calls: create a client, `transform()` the input, `reverse()` the output. TypeScript first; Python and REST are planned. [Register for early access](https://nakato.ai/developers).

### About us

Founded in 2026 by Tom Fairey (Founder and CEO) and Sam Weston (Co-founder and CTO). Headquartered in London, with an office in New York.

### Find out more

- [How it works](https://nakato.ai/how-it-works)
- [Assurance and regulation](https://nakato.ai/assurance) (built against UK GDPR, EU GDPR, the EU AI Act and DORA)
- [Insights](https://nakato.ai/insights)
- [Talk to us](https://nakato.ai/contact)

London and New York · [nakato.ai](https://nakato.ai)

<sub>Nakato is a trading name of Presential Limited, registered in England and Wales, company number 17039008.</sub>
