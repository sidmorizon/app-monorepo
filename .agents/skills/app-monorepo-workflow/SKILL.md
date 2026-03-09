# app-monorepo Upstream PR Workflow

This skill documents the required workflow for working with the `sidmorizon/app-monorepo` repository.

## Rules (MUST follow every time)

1. **Always sync from upstream before starting work:**
   ```bash
   cd ~/repos/app-monorepo
   git remote add upstream https://git-manager.devin.ai/proxy/github.com/OneKeyHQ/app-monorepo 2>/dev/null || true
   git fetch upstream x
   git checkout x
   git merge upstream/x
   git push origin x
   ```

2. **Always submit PRs to the upstream repo (`OneKeyHQ/app-monorepo`), NOT to the fork (`sidmorizon/app-monorepo`):**
   - Push your branch to `origin` (sidmorizon/app-monorepo)
   - Create the PR with:
     - `repo`: `OneKeyHQ/app-monorepo`
     - `head_branch`: `sidmorizon:<your-branch-name>`
     - `base_branch`: `x`
   - Note: This requires write access to `OneKeyHQ/app-monorepo`. If you don't have access, ask the user to either grant access or create the cross-fork PR manually.

3. **The default/main branch is `x`** (not `main` or `master`).

## Branch Naming

Follow the standard convention: `devin/{timestamp}-{descriptive-slug}`
