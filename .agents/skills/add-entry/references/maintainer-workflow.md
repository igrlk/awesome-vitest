# Maintainer Workflow

## Suggest Category Changes

When a supplied resource exposes a placement issue, suggest a new category or a relevant rename, split, merge, or reassignment of existing entries when useful. Keep proposals tied to that resource and within the [category organization rules](../../../../AGENTS.md#category-organization), rather than auditing the inventory.

Explain the placement problem and the proposed change, keeping this skill’s category work limited to proposals. Applying and committing a proposal requires separately approved work through the applicable change and commit workflows. If an entry depends on it, defer the addition until the category change is committed. Keep category changes out of the addition commit.

## Credit Entry Authors

Identify whom to credit for each committed resource, reusing evidence from its assessment. Do not conduct a separate attribution lookup for assessment or wording-only requests. Attribution uncertainty does not prevent an otherwise approved addition from being committed.

Seek the author or originator of the specific resource. Keep that role distinct from its current maintainer, declared code owner, and repository owner. Evidence must establish who did what, not merely who is involved.

### Resolve Resource Identity

Establish the canonical repository and the relevant package or component. Inspect the package’s own manifest rather than assuming a root manifest describes it. For npm packages, [`repository.directory`](https://docs.npmjs.com/cli/v12/configuring-npm/package-json/#repository) can locate the package inside a monorepo. Retain discovered former names, directory moves, repository transfers, and predecessor projects when relevant to tracing origin.

### Find Direct Attribution

Start with the package manifest, package-specific README credits, and authors or maintainer files. npm’s [`author` and `contributors` fields](https://docs.npmjs.com/cli/v12/configuring-npm/package-json/#people-fields-author-contributors) are distinct from registry maintainer metadata. A declared author is not necessarily the sole creator or current maintainer, and organizational credit does not identify an individual. npm can derive `contributors` from an `AUTHORS` file, so those sources may repeat the same credit rather than corroborate it independently.

When a person is explicitly credited as an author, verify their GitHub account and stop if that resolves the attribution. Do not reconstruct the entire history unnecessarily.

### Verify GitHub Accounts

Prefer an explicit GitHub profile link or GitHub’s account association on a relevant commit. In [REST commit responses](https://docs.github.com/en/rest/commits/commits#list-commits), distinguish raw `commit.author` metadata from the associated account in `author.login` and from the separate committer fields. Use the author association as evidence, not an assumption of sole authorship. Do not infer a handle from a matching real name, email prefix, or npm username.

Inspect a pull request’s contribution before assigning credit. Opening or merging it does not establish sole implementation authorship. Preserve substantive coauthorship, including work submitted or merged through automation.

### Trace Origin When Needed

If direct attribution is missing or ambiguous, inspect package-specific implementation history and relevant pull requests within a bounded scope. Filter commits by the relevant path and branch. Account for pagination rather than treating one page as complete history. Follow discovered predecessor paths when needed, without assuming path filtering follows renames automatically.

Find the change that introduced the actual integration, distinguishing original implementation from a rename, relocation, fork import, or bulk migration. Stop when the evidence supports attribution. Do not use a fixed score or rank people by commit count. Discount dependency bumps, formatting sweeps, release automation, generated changes, and unrelated monorepo work without discarding substantive coauthorship.

### Distinguish Other Roles

Do not substitute a maintainer or code owner when an individual author cannot be established. Recent substantive package work can support a **likely maintainer** inference, not a verified designation or original-author credit. Keep that qualification when relevant to explaining the result.

Inspect ownership rules only when they resolve a material ambiguity. [GitHub code ownership](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) assigns review responsibility, not original authorship. On the relevant branch, GitHub uses the first file found in this order: `.github/CODEOWNERS`, root `CODEOWNERS`, then `docs/CODEOWNERS`. Within that file, the last matching pattern wins. Evaluate relevant implementation files, not only the manifest. Preserve differing file owners, follow a documented custom ownership system’s semantics when applicable, and never choose an arbitrary member of a team.

### Deliver Greeting

For each committed entry with verified individual author accounts, identify the resource and output one greeting in its own fenced code block, replacing the placeholder with the verified handle:

```text
👋 @<author-handle>
```

For multiple supported authors, place their handles alphabetically on the same greeting line, separated by single spaces. Outside the block, give the supported attribution role and decisive evidence link. Include competing attribution or a limitation only when it materially affects whom to credit.

If only an organization, team, unverified identity, or insufficient evidence is available, omit the greeting and explain the limitation. Inaccessible evidence does not prove that no author exists. Do not present a likely maintainer as an author merely to produce a mention.

The greeting is output for the user to copy. Do not post a comment, notify anyone remotely, or publish the commit without separate authorization.
