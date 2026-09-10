# FlyHub `.github` update

This bundle aligns the organization-level GitHub templates with the current delivery model:

```text
Milestone
→ Parent Issue
→ Sub-issues
→ logical commits
→ one Pull Request
→ Rebase and merge
→ main
```

## Files

- `PULL_REQUEST_TEMPLATE.md`
- `ISSUE_TEMPLATE/feature-task.yml`
- `ISSUE_TEMPLATE/bug.yml`

No separate Parent Issue or Sub-issue template is introduced. The shared `Feature / Task` template supports both through GitHub's native Sub-issues relationship.

## Repository settings

Repository settings are not represented by files.

For repositories using this workflow:

1. allow **Rebase and merge**;
2. configure the `main` ruleset to allow **rebase** as the merge method;
3. keep **Require linear history** enabled;
4. keep pull requests required for `main`;
5. keep force pushes and deletion of `main` blocked;
6. keep automatic deletion of merged head branches enabled when appropriate.

`Squash and merge` should not be the normal merge method for Parent Issue deliveries because it would collapse the Sub-issue commits that the process intends to preserve.
