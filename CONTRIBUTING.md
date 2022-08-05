# Contributing

Contributions are welcome and will be fully credited!

We accept contributions via Pull Requests.

## Pull Requests
Each Pull Request name should meet following RegExp: `\[(major|minor|path|internal)\]\s(.+)`. Example:
```
[patch] Fix something
```

Here are some guidelines to make the process smoother:

- **Add a test** - New features and bugfixes need tests. If you find it difficult to test, please tell us in the pull request and we will try to help you!
- **Document any change in behaviour** - Make sure the `README.md` and any other relevant documentation are kept up-to-date.
- **Run `npm test` locally** - This will allow you to go faster
- **One pull request per feature** - If you want to do more than one thing, send multiple pull requests.
- **Send coherent history** - Make sure your commits message means something
- **Consider our release cycle** - We try to follow [SemVer v2.0.0](http://semver.org/). Randomly breaking public APIs is not an option.

## Git Commit Message Convention

> This is adapted from [Vue's commit convention](https://github.com/vuejs/core/blob/a95554d35c65e5bfd0bf9d1c5b908ae789345a6d/.github/commit-convention.md).

#### TL;DR:

Messages must be matched by the following regex:

```js
;/^(revert: )?(feat|fix|docs|dx|style|refactor|perf|test|workflow|build|ci|chore|types|wip)(\(.+\))?: .{1,50}/
```

#### Examples

Appears under "Features" header, `compiler` subheader:

```
feat(compiler): add 'comments' option
```

Appears under "Bug Fixes" header, `v-model` subheader, with a link to issue #28:

```
fix(v-model): handle events on blur

close #28
```

Appears under "Performance Improvements" header, and under "Breaking Changes" with the breaking change explanation:

```
perf(core): improve vdom diffing by removing 'foo' option

BREAKING CHANGE: The 'foo' option has been removed.
```

The following commit and commit `667ecc1` do not appear in the changelog if they are under the same release. If not, the revert commit appears under the "Reverts" header.

```
revert: feat(compiler): add 'comments' option

This reverts commit 667ecc1654a317a13331b17617d973392f415f02.
```

### Full Message Format

A commit message consists of a **header**, **body** and **footer**. The header has a **type**, **scope** and **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

### Revert

If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit. In the body, it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type

If the prefix is `feat`, `fix` or `perf`, it will appear in the changelog. However, if there is any [BREAKING CHANGE](#footer), the commit will always appear in the changelog.

Other prefixes are up to your discretion. Suggested prefixes are `docs`, `chore`, `style`, `refactor`, and `test` for non-changelog related tasks.

### Scope

The scope could be anything specifying the place of the commit change. For example `core`, `compiler`, `ssr`, `v-model`, `transition` etc...

### Subject

The subject contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize the first letter
- no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

## Creating issues

### Bug reports

Always try to provide as much information as possible. If you are reporting a bug, try to provide a repro on jsfiddle.net (or anything else) or a stacktrace at the very least. This will help us check the problem quicker.

### Feature requests

Lay out the reasoning behind it and propose an API for it. Ideally, you should have a practical example to prove the utility of the feature you're requesting.
