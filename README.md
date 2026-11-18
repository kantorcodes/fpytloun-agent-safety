# Awesome Agent Safety [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, frameworks, research, and resources for making AI agents safe and governable.

AI agents are executing real-world actions — file operations, API calls, database queries, financial transactions. This list covers tools that help developers control what agents can do, detect when they go wrong, and maintain audit trails for compliance.

## Contents

- [Policy Engines & Authorization](#policy-engines--authorization)
- [Content Safety & Guardrails](#content-safety--guardrails)
- [MCP Security](#mcp-security)
- [Audit & Compliance](#audit--compliance)
- [Monitoring & Observability](#monitoring--observability)
- [Red Teaming & Testing](#red-teaming--testing)
- [Standards & Frameworks](#standards--frameworks)
- [Research Papers](#research-papers)
- [Articles & Blog Posts](#articles--blog-posts)
- [Contributing](#contributing)

## Policy Engines & Authorization

Tools that control what actions AI agents are allowed to take.

- [Authensor](https://github.com/authensor/authensor) - Open-source safety stack with policy engine, approval workflows, content scanning, cryptographic audit trail, and MCP governance. MIT licensed.
- [AWS Cedar](https://github.com/cedar-policy/cedar) - Policy language for authorization, used in AWS AgentCore. Apache 2.0.
- [Galileo Agent Control](https://github.com/rungalileo/agent-control) - Centralized policy engine for agent runtime governance. Apache 2.0.
- [HOL Guard](https://hol.org/guard) - Local policy checks and approvals for supported AI coding-agent shell, file, package, and MCP actions. Apache 2.0.
- [Permit.io](https://www.permit.io/) - Fine-grained authorization for AI agents with ReBAC and ABAC support (commercial).
- [AgenticContract](https://github.com/agenticcontract/agenticcontract) - Enforceable rules, risk limits, and obligation tracking for agents. Rust core.
- [OPA (Open Policy Agent)](https://github.com/open-policy-agent/opa) - General-purpose policy engine, increasingly used for agent authorization. Apache 2.0.

## Content Safety & Guardrails

Tools that scan agent inputs/outputs for threats.

- [Authensor Aegis](https://github.com/authensor/authensor/tree/main/packages/aegis) - Zero-dependency content scanner for prompt injection, PII, credentials, and memory poisoning. MIT.
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - Programmable guardrails using Colang for conversational AI. Apache 2.0.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - I/O validation framework with 300+ community validators. Apache 2.0.
- [LLM Guard](https://github.com/protectai/llm-guard) - Input/output scanners for prompt injection, PII, and toxicity. Apache 2.0.
- [Rebuff](https://github.com/protectai/rebuff) - Self-hardening prompt injection detection. Apache 2.0.
- [Lakera Guard](https://www.lakera.ai/) - Real-time prompt injection defense (acquired by Check Point).
- [Lasso Security](https://www.lasso.security/) - Triple-gate pattern for MCP + LLM + API layer protection.
- [Vigil](https://github.com/deadbits/vigil-llm) - LLM prompt injection detection with heuristic + ML scoring. MIT.
- [Prompt Armor](https://promptarmor.com/) - Prompt injection detection API with real-time scanning (commercial).

## MCP Security

Tools specifically for securing Model Context Protocol servers.

- [Authensor MCP Gateway](https://github.com/authensor/authensor/tree/main/packages/mcp-server) - Policy enforcement proxy for MCP tool calls with approval workflows. MIT.
- [mcp-context-protector](https://github.com/trailofbits/mcp-context-protector) - Trust-on-first-use pinning + injection scanning for MCP. Trail of Bits.
- [MintMCP](https://www.mintmcp.com/) - Managed MCP gateway with OAuth/SSO and access controls (commercial).
- [Operant AI](https://www.operant.ai/) - MCP gateway with Shadow Escape detection and runtime protection.
- [Invariant Labs MCP Scanner](https://github.com/invariantlabs-ai/mcp-scan) - Static analysis scanner for MCP server vulnerabilities.

## Audit & Compliance

Tools for maintaining audit trails and regulatory compliance.

- [Authensor Receipts](https://github.com/authensor/authensor/tree/main/packages/control-plane) - SHA-256 hash-chained tamper-evident audit trail. EU AI Act Article 12 compatible. MIT.
- [Sigstore](https://sigstore.dev/) - Keyless software signing and transparency logs. Can be used for agent action attestation.
- [in-toto](https://github.com/in-toto/in-toto) - Framework for securing software supply chains with verifiable metadata. Apache 2.0.

## Monitoring & Observability

Tools for detecting anomalous agent behavior.

- [Authensor Sentinel](https://github.com/authensor/authensor/tree/main/packages/sentinel) - EWMA/CUSUM behavioral anomaly detection engine. Zero dependencies. MIT.
- [Arthur AI](https://www.arthur.ai/) - AI monitoring, evaluation, and observability platform (commercial).
- [Cisco AI Defense](https://www.cisco.com/site/us/en/products/security/ai-defense/) - Enterprise AI runtime protection (acquired Robust Intelligence).
- [Langfuse](https://github.com/langfuse/langfuse) - Open-source LLM observability with tracing, evaluation, and prompt management. MIT.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source observability for LLM applications with trace analysis. Apache 2.0.
- [WhyLabs](https://www.whylabs.ai/) - AI observability with drift detection and data quality monitoring (commercial).

## Red Teaming & Testing

Tools for testing agent safety and finding vulnerabilities.

- [Chainbreaker](https://github.com/15researchlab/chainbreaker) - AI red-teaming workbench. Multi-step attack chains, ATLAS TTPs, MCP scanning. MIT.
- [Garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner with probe-based architecture. Apache 2.0.
- [PyRIT](https://github.com/Azure/PyRIT) - Python Risk Identification Toolkit for generative AI. Microsoft. MIT.
- [Gandalf](https://gandalf.lakera.ai/) - Interactive prompt injection challenge for testing defense strategies (Lakera/Check Point).
- [Promptfoo](https://github.com/promptfoo/promptfoo) - LLM testing and red-teaming with automated vulnerability scanning. MIT.
- [Counterfit](https://github.com/Azure/counterfit) - CLI tool for assessing the security of ML models. Microsoft. MIT.

## Standards & Frameworks

Industry standards and regulatory frameworks relevant to agent safety.

- [OWASP Top 10 for Agentic Applications (2026)](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications/) - 10 critical risks for agentic AI applications.
- [EU AI Act](https://artificialintelligenceact.eu/) - European regulation for AI systems. High-risk AI system deadline: August 2, 2026.
- [NIST AI 600-1](https://csrc.nist.gov/publications/detail/ai/600-1/final) - AI Risk Management Framework: Generative AI Profile.
- [ISO/IEC 42001](https://www.iso.org/standard/81230.html) - AI Management System standard for organizational AI governance.
- [MITRE ATLAS](https://atlas.mitre.org/) - Adversarial Threat Landscape for AI Systems. Threat modeling framework.
- [OWASP MCP Top 10](https://genai.owasp.org/) - Security risks specific to Model Context Protocol.
- [NIST SP 800-218A](https://csrc.nist.gov/pubs/sp/800/218/a/final) - Secure Software Development Practices for Generative AI and Dual-Use Foundation Models.

## Research Papers

- [Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/abs/2302.12173) - Foundational work on indirect prompt injection attacks.
- [MINJA: Jailbreaking LLMs via Memory INJection Attacks](https://arxiv.org/abs/2410.21497) - Memory poisoning attacks against RAG-augmented LLMs.
- [Toolshed: Scale Tool-Equipped Agents with Advanced RAG-Tool Fusion](https://arxiv.org/abs/2410.14594) - Research on scaling tool use while maintaining safety.
- [Agent Security Bench (ASB)](https://arxiv.org/abs/2410.02644) - Comprehensive benchmark for evaluating LLM agent security across attack scenarios.
- [AgentDojo: A Dynamic Environment to Evaluate Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) - Framework for evaluating agent safety in realistic scenarios.

## Articles & Blog Posts

- [Why Agent Safety Should Be Free](https://authensor.com/updates/why-agent-safety-should-be-free) - The case for open-source safety tooling.
- [OWASP Agentic Top 10 Explained](https://authensor.com/updates/owasp-agentic-top-10-explained) - Walkthrough of all 10 risks with mitigation strategies.
- [MCP Server Authorization](https://authensor.com/updates/mcp-server-authorization) - Why MCP needs an authorization layer.
- [Anthropic: Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) - Patterns and principles for building reliable AI agents.
- [Simon Willison: Prompt Injection](https://simonwillison.net/series/prompt-injection/) - Running series on prompt injection risks and mitigations.
- [Trail of Bits: MCP Security](https://blog.trailofbits.com/2025/04/23/mcp-security-notification-tool-poisoning-attacks/) - Analysis of MCP tool poisoning attack vectors.

## Contributing

Contributions welcome! Please read the [contributing guidelines](CONTRIBUTING.md) before submitting a PR.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
