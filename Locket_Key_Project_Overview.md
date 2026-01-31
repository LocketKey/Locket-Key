Locket Key Project Overview
Executive Summary
Locket Key is a privacy-first, offline AI platform designed for technologically illiterate users—primarily seniors and digital outsiders. It transforms complex AI capabilities into an accessible, secure "digital workshop" through device-bound encryption, pedagogical interface design, and local-first execution.
Core Philosophy: "Sovereign Simplicity"

Absolute privacy through offline-only operation
Hardware-locked encryption (TPM/Secure Enclave)
Educational scaffolding that teaches through use
Physical metaphors replacing technical abstractions


Product Strategy & Technical Architecture
Value Proposition Pillars

Sovereignty: Zero telemetry, air-gapped local execution
Accessibility: Guided interactions for non-technical users
Security: Device-bound encryption renders data useless if stolen

Technical Stack
ComponentTechnologyRationaleFrontendElectron + ReactCross-platform desktop app with rich UI capabilitiesBackendPython (FastAPI)Native AI ecosystem integrationInferencellama.cpp (GGUF)Best performance on consumer hardwareDatabaseSQLite + SQLCipherServerless, encrypted, portableSecurityTPM 2.0 / Secure EnclaveHardware-backed key storage
Model Strategy
Tiered Deployment:

8GB RAM: Small Language Models (Phi-3, Gemma 2B)
16GB RAM: Llama 3 8B, Mistral 7B (Q4_K_M quantization)
32GB+ RAM: Larger models with full context windows

Interchangeable Design:

OpenAI API-compatible abstraction layer
Hot-swappable inference backends (Ollama, vLLM)
Model Context Protocol (MCP) for data source integration

Multi-Agent Architecture
Serial Orchestration Pattern:
User Request → Chief of Staff (Router)
              ↓
         Task Delegation
              ↓
    ┌────────┴────────┐
    ↓                 ↓
The Researcher    The Scribe
(RAG Agent)       (Writer)
    ↓                 ↓
    └────────┬────────┘
             ↓
      The Guard (Privacy)
             ↓
      Unified Response
Why Serial? Single GPU systems cannot run parallel agents. Sequential execution with visible process tracking builds trust and manages latency expectations.

User Experience Research & Design Principles
Target User Profile: "The Reluctant Adopter"
Characteristics:

High trust deficit from dark patterns and scams
Fear of irreversible mistakes ("I'll break it")
Desire for independence, not dependency
Lacks mental models for file systems, cloud storage
Suffers from "blank page" anxiety with AI prompts

Core UX Paradigms
1. Neoskeuomorphic Design
Physical-world metaphors replace abstract concepts:
Technical ConceptUser MetaphorVisualEncryption"The Locket"Golden padlock, wax sealPrivate Key"Master Key"Ornate physical keyOffline Mode"The Vault"Thick border, disconnected plug iconModel Weights"Brain Cartridge"Physical cartridge insertionContext Window"Notepad"Filling pages metaphor
2. Staff Meeting Orchestration
AI agents visualized as a digital team:

The Concierge: Primary interface, delegates tasks
The Scribe: Writing specialist
The Clerk: Math and logic
The Guard: Privacy/safety monitor

Users watch agents "work" in sequence, demystifying latency and building trust.
3. Pedagogical Scaffolding
Progressive Disclosure Phases:

Novice: Restricted UI with guided wizards
Apprentice: Revealed controls (tone, style)
Master: Full model swapping, fine-tuning access

"Flip & Discover" Method:
Instead of demanding prompts, AI interviews the user:

"I see you want to write a letter. Who is it for? What's the tone—serious or friendly?"

This implicitly teaches prompt engineering through conversation.
4. Accessibility Standards
ElementRequirementWhyTypography18px min, Atkinson HyperlegibleAging eyes, cataractsContrast7:1 (WCAG AAA)Maximum definitionTouch Targets44x44px minimumTremors, motor controlFeedbackVisual + Haptic + AudioMulti-sensory reinforcement
Anti-Dark Pattern Philosophy

Honest Defaults: Privacy-first, no opt-out tracking
Visual Stability: No layout shifts
Explicit Exits: Always-visible "Go Home" button
Massive Undo: Always-accessible reversal of actions


Market Analysis & Competitive Landscape
Market Opportunity: The "Digital Divide"
Underserved Demographic:

40M+ seniors in US alone (growing to 80M by 2040)
Privacy-conscious professionals opting out of surveillance economy
Non-digital professions (trades, healthcare, education)

Pain Points:

Cloud AI demands unacceptable privacy trade-offs
Local tools (Ollama, LM Studio) require CLI expertise
AI PCs still cloud-hybrid, OS-tethered telemetry

Competitive Matrix
ProductInterfaceTargetOfflineEducationalSecurityOllamaCLI/APIDevelopers✓✗TransportLM StudioComplex GUIPower Users✓✗TransportGPT4AllSimple GUIGeneral✓✗StandardApple IntelligenceSystem IntegrationApple UsersHybrid✗HighMicrosoft Copilot+OS IntegrationEnterpriseHybrid✗MediumLocket KeyVoice/Visual MetaphorTech Illiterate✓ Strict✓ Integrated Tutor✓ Device-Bound
Market Positioning
Differentiation:

Only truly offline consumer AI (air-gapped by default)
Hardware-locked encryption (TPM/Secure Enclave)
Pedagogical interface that teaches AI literacy
Privacy as the product, not the feature

Marketing Position:

"Your Secrets, Your Key. The AI that lives only on your computer."

Strategic Timing (2026 Window)
Convergence Factors:

NPU Ubiquity: 60% faster inference, 44% less power than GPU
SLM Maturation: Qwen3, DeepSeek-V3 rival larger models
MCP Standardization: Universal data source protocol
Privacy Backlash: Cloud AI data breaches fueling demand

Threat Analysis: The "Scam Shield" Positioning
"Grandparent Scam" Epidemic:

Fraud cases doubled (79K→150K in Canada)
AI voice cloning weaponized against seniors

Locket Key Response:

Local "Guardian Mode" analyzes calls/emails for fraud markers
No data leaves device, provides real-time "Safe/Danger" indicators
Positions product as defensive necessity, not luxury


Development Roadmap
Phase 1: The Digital Safe (Q3 2025)

Encrypted file organization (TPM/Secure Enclave)
Basic RAG with Phi-3 model
"Chat with your Locket" functionality

Phase 2: The Educational Companion (Q1 2026)

"Mad Libs" prompting interface
Voice-first interaction (local Whisper)
Tutor agent for guided learning

Phase 3: The Guardian Agent (Q3 2026)

Proactive scam detection
Full MCP integration for local tasks
Multi-agent orchestration (Planner, Researcher, Writer, Reviewer)


Implementation Principles
Design Commandments

Never expose file paths - Use spatial/visual browsing
Never show technical errors - Translate to plain language
Always provide "Undo" - Visible, persistent safety net
Always explain latency - Show agents "working," not spinning wheels
Never hide complexity - Make it visible but comprehensible through metaphor

Success Metrics

Trust: Can user explain where their data lives?
Competence: Can user swap models without documentation?
Independence: Can user recover from errors unassisted?
Learning: Does usage decrease reliance on "wizards" over time?


Technical Dependencies
Hardware Requirements:

Minimum: 16GB RAM, NPU-enabled processor
Optimal: 32GB RAM, dedicated NPU, NVMe SSD
Platforms: Windows 10+ (TPM 2.0), macOS (Apple Silicon)

Model Ecosystem:

Primary: Qwen3 series, Llama 3, Mistral
Specialized: Qwen3-Coder (development tasks)
Router: Phi-3 Mini (NPU-resident)


Repository Structure
locket-key/
├── docs/
│   ├── product-strategy.md (this file)
│   ├── ux-research.md
│   └── market-analysis.md
├── src/
│   ├── frontend/          # Electron + React
│   ├── backend/           # FastAPI + Orchestration
│   ├── inference/         # llama.cpp bindings
│   └── security/          # TPM/Secure Enclave integration
├── models/                # GGUF model storage
└── README.md

Contact & Contribution
This is a private research project. For inquiries regarding the Locket Key vision and implementation, please reference the comprehensive strategy documents in /docs.
Project Philosophy:
"Technology should adapt to humans, not humans to technology."
