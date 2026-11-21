# AI Football Agents — Amazon EMEA Early Career Talent Hackathon (Oct 2026)

Based on the official AWS **AI Possibilities Samples** repository ([`aws-samples/sample-ai-possibilities`](https://github.com/aws-samples/sample-ai-possibilities)), which showcases experimental AI prototypes and demos built with AWS services. I forked the initial AWS agentic football templates and customized/improved them for the **Amazon EMEA Early Career Talent Hackathon (Oct 2026)**.

## Key Customizations & Engineering Highlights
- **5-Agent Team Architecture:** Built and deployed solo a 5-agent football team on **Amazon Bedrock (Nova)**, **AgentCore**, and **Strands**, starting from the base AWS templates.
- **Structured Prompt Engineering:** Rewrote all 5 system prompts as ordered decision rules with role-limited commands, strict valid parameter ranges, and safe defaults. Leveraged **Kiro** and **Claude** for iterative design and debugging, enforcing `py_compile` syntax checks before every redeployment.
- **Latency & Behavior Optimization:** Diagnosed production issues via **Amazon CloudWatch** logs—traced a `1.5 s` mean decision latency (against a `500 ms` limit) caused by excessive tool calls on nearly every game tick, and resolved goalkeeper realism-check failures by restricting its available commands and removing unnecessary memory overhead.

> ⚠️ **Note:** Like the upstream AWS samples, this repository is an experimental proof-of-concept built for hackathon demonstration and learning purposes, not a production-ready deployment.
