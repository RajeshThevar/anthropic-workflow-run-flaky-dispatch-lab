# A-008 Workflow-Run Flaky Dispatch Lab

This disposable lab models the official `examples/test-failure-analysis.yml`
pattern from `anthropics/claude-code-action`.

Goal:

- Trigger a failing `CI` run from a fork-origin pull request.
- Let a downstream `workflow_run` job run in the base repository context.
- Use a fake Claude executable, dummy Anthropic auth, and sanitized structured
  output.
- Observe whether the downstream job can use `actions: write` to dispatch the
  base repository `CI` workflow on the attacker-chosen `head_branch`.

No real Anthropic credentials, customer data, or third-party targets are used.

