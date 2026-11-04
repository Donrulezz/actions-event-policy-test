# actions-event-policy-test

Test repository for a deadlinefix.com guide (November 2026): how GitHub Actions event policies behave, and what a run blocked by an event policy looks like.

- `.github/workflows/ci.yml` runs on `push` and `workflow_dispatch`.
- Run #1 was blocked by a repository event policy that allowed only `pull_request_target`: startup failure, annotation `Event 'push' is not allowed to trigger Actions workflows.`
- After the policy also allowed `push` and `workflow_dispatch`, the workflow ran again.
