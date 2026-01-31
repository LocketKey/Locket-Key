# Locket Key: Privacy-First AI for Digital Accessibility

> Offline, device-bound AI designed for seniors and technologically illiterate users

## The Problem

- 75% of seniors use technology, but only 25% feel confident (AARP)
- Seniors lose $1.5B annually to fraud (FTC)
- Current AI tools require cloud connectivity, sacrificing privacy
- Existing interfaces assume digital literacy and comfort with abstractions

## The Solution

Locket Key is a local-first AI interface that:
- Runs entirely offline (no data ever leaves the device)
- Uses device-bound encryption (TPM/Secure Enclave)
- Provides pedagogical guidance (teaches users how to interact with AI)
- Employs skeuomorphic design (physical-world metaphors)
- Protects against scams through local monitoring

## Current Status

**Research & Development Phase** - seeking funding to build initial prototype

We're developing:
- Privacy architecture using hardware-backed encryption
- Multi-agent orchestration for complex tasks
- Accessible interface design for low-literacy users
- Local RAG (Retrieval-Augmented Generation) implementation

## Roadmap

**Phase 1: The Digital Safe** (Planned)
- Encrypted local file organization
- Basic chat interface with local LLM
- Voice-first interaction

**Phase 2: The Educational Companion** (Planned)
- Guided prompting interface ("wizards")
- Text-to-speech integration
- Progressive disclosure learning system

**Phase 3: The Guardian Agent** (Planned)
- Scam detection and protection
- Multi-agent task automation
- Model Context Protocol integration

## Technical Approach

- **Models**: Small Language Models (Qwen, Phi, Llama) via GGUF quantization
- **Security**: TPM 2.0 (Windows) / Secure Enclave (macOS) for device-bound keys
- **Inference**: Local execution via llama.cpp / Ollama
- **Interface**: Electron + React with neoskeuomorphic design
- **Architecture**: Model-agnostic abstraction layer for interchangeability

## Documentation

See `/docs` folder for detailed strategy documents covering:
- Product strategy and technical architecture
- User experience research and design principles
- Market analysis and competitive landscape

## Funding

This project is seeking funding through grants and community support. See [FUNDING.md](FUNDING.md) for details

## Contact

Email: Locket.Key.LLC@Proton.me

---

*Building sovereign AI for the digital outsider.*
