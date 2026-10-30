## Orlando Becerra

I build and run LLM agents in production: the agent loop, tools, evals, guardrails, cost and reliability, on Claude and AWS Bedrock. Staff Software Engineer at Apploi, with 14+ years in backend and distributed systems. Based in Madrid, Spain.

### What I work on

- **Candidate-facing AI agent (technical owner).** A streaming Claude agent on AWS Bedrock with 29 tools. It screens job candidates over SMS and email, answers their questions and books interviews on recruiters' Google and Microsoft calendars. In October 2026 it handled ~2.4K applications, ~14K turns and ~41K tool calls at 97%+ turn success, with 99% of input tokens served from prompt cache.
- **Ada, an internal Claude data agent (core engineer).** Natural language to SQL over Snowflake, answered in Slack, used by ~60 employees a month. I helped take it from early concept to production: ECS Fargate deployment, prompt caching and cost tracking, a Claude Haiku LLM-as-judge feedback loop, the move to AWS Bedrock, sandboxed code execution and agent-to-agent (A2A) tools.
- **Safety and evals.** Fail-closed Bedrock Guardrails with prompt-injection detection, a save-time LLM review of recruiter-written instructions with quote verification, and regression evals built from 3 production incidents, run by hand after prompt or model changes.
- **Reliability.** Co-designed and implemented the fix for a production incident where conflicting workflow instructions and concurrent turns forked conversations: a per-conversation turn lease, one precedence rule and an LLM conflict check that escalates to a human. Forked turns fell from 2.2% to 0 while volume tripled.
- **AWS serverless.** Led the move of 100+ background tasks onto EventBridge, SQS and Lambda, now ~16M invocations a month. Built enterprise SSO and an email service sending ~4.5M emails a month.
- **AI-assisted development.** Designed my team's Claude Code workflow: spec, tickets, TDD, parallel agents in git worktrees, two code reviews and a live test before merge.

That work lives in private company repositories; the public repos here are mostly older projects and forks.

### Stack

- **AI:** Anthropic Claude, Amazon Bedrock (AgentCore, Guardrails), tool use, streaming, structured output, prompt caching, evals and LLM-as-judge
- **Backend:** Python (FastAPI, Flask, Django), SQLAlchemy, REST and GraphQL
- **AWS:** Lambda, EventBridge, SQS, ECS Fargate, Cognito, S3
- **Infrastructure:** Terraform, AWS SAM, GitHub Actions
- **Data:** Snowflake, PostgreSQL, MySQL, MongoDB
- **Tools:** Claude Code

### Open source

- [pallets-eco/flask-sqlalchemy#1202](https://github.com/pallets-eco/flask-sqlalchemy/pull/1202): `Pagination.next()` dropped `max_per_page`, so the next page came back with the wrong `per_page`. Wrote a failing regression test first, then the fix; merged by the maintainers and released in Flask-SQLAlchemy 3.0.5 (June 2023).

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/orlandobcrra)
