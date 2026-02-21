# Contributing to Agent Factory Reference

Thank you for considering a contribution! This guide is a community effort, and your help makes it better for everyone.

---

## Before You Contribute

Please read:
- The [full reference guide](AGENT_FACTORY_REFERENCE.md) to understand the format and scope
- The [disclaimer](AGENT_FACTORY_REFERENCE.md#️-disclaimer) to understand what this guide is and isn't

---

## What We're Looking For

### High-Value Contributions

| Type | Example | Impact |
|------|---------|--------|
| **Production experience** | "We deployed X at Y hospital, here's what worked" | 🔴 Very High |
| **Compliance mappings** | "Tool X addresses HIPAA requirement Y because..." | 🔴 Very High |
| **Outdated resource flags** | "Repo X hasn't been updated since 2024" | 🟡 Medium |
| **New tool additions** | "Here's a new MCP server for Z" | 🟡 Medium |
| **Broken link fixes** | "This link is dead, here's the new one" | 🟢 Quick Win |

### What We Don't Want

- **Self-promotion without substance** — your company's tool is fine, but describe it objectively
- **Vaporware** — tools that exist only in press releases
- **Unverified tools** — you should have actually used it
- **Generic AI tools** — we focus on regulated industries specifically

---

## How to Contribute

### Option 1: File an Issue

Best for:
- Reporting outdated or broken links
- Flagging incorrect information
- Suggesting resources you haven't fully evaluated
- Asking questions

### Option 2: Open a Pull Request

Best for:
- Adding new resources with descriptions
- Fixing errors in existing entries
- Improving documentation

---

## Contribution Format

### Adding a New Resource

Follow this format:

```markdown
**[Tool Name](https://github.com/org/repo)**
> _One-line description of what it does_

Two to three sentences explaining:
1. What problem it solves
2. Who should use it
3. Any important limitations or considerations
```

Example:
```markdown
**[FinGPT](https://github.com/AI4Finance-Foundation/FinGPT)**
> _Open-source financial LLMs with continuous fine-tuning pipelines_

The standout feature isn't the models themselves — it's the continuous update mechanism. Financial markets are relentlessly current; a model trained six months ago on earnings calls is already stale. Most relevant for sentiment analysis agents and market intelligence tools.
```

### Key Principles

1. **Plain language** — no marketing speak, no buzzwords
2. **Honest limitations** — every tool has them; mention them
3. **Compliance relevance** — explain why it matters for regulated industries
4. **Verified use** — describe your actual experience when possible

---

## Pull Request Checklist

Before submitting:

- [ ] I've verified the resource is actively maintained (check last commit date)
- [ ] I've actually used this resource (or cited someone who has)
- [ ] My description follows the format above
- [ ] I've placed the resource in the correct section
- [ ] I've noted any compliance considerations
- [ ] I've checked for duplicate entries

---

## Review Process

1. **Automated checks**: Links are verified to be accessible
2. **Maintainer review**: Entries are evaluated for quality and relevance
3. **Community feedback**: High-impact additions may be discussed in GitHub Discussions
4. **Merge**: Approved PRs are merged and credited in the update log

---

## Recognition

Contributors who make consistent, high-quality contributions over 6+ months will be:
- Listed as co-curators in the reference guide
- Credited in the update log
- Acknowledged in the README

---

## Code of Conduct

- Be respectful and constructive
- Focus on helping the community
- Disclose any conflicts of interest
- Prioritize quality over quantity

---

## Questions?

- **GitHub Issues**: For specific problems or suggestions
- **GitHub Discussions**: For broader conversations
- **LinkedIn**: Connect with Mario Lazo for direct feedback

---

Thank you for making this resource better! 🙏
