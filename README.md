# Reproduction steps

1. Run `pnpm install`.
2. Observe lockfile doesn't change since it is already up to date.
3. `pnpm install --frozen-lockfile`
4. **Expected:** Install should succeed.

   **Actual:** Fails with the following error:
   ```
   ERR_PNPM_OUTDATED_LOCKFILE  Cannot install with "frozen-lockfile" because pnpm-lock.yaml is not up-to-date with package.json
   ```
