# Commit naming

In Nukomeet we use very strict commit naming convention that help us with further reviewing `git log`.

## Template

Template that we use looks like:

```
<commit type>: <short description>

<further, longer description>

<issues relationship> [<work time>]
```

Don't worry if it looks complicated. Only some of this fields are required and it is very easy to get used to.

### Commit types (required)

To allow us to extract what was type of commit we begins our commit messages with commit type tag. There are a few of them:

| Name     | Description |
| -------- | ----------- |
| `improv` | Refactoring and code style improvements |
| `feat`   | New features |
| `fix`     | Code fixes |
| `docs`   | Documentation |
| `style`  | CSS styling |
| `test`   | Testing |

## Short description (required)

This is place where you should add short description of Your work. No more than 60-70 characters. Be precise but laconic, do not write poems here, but leave reviewer clean message about reason of this changes. If you are poet, then you will have time for it later.

**Good examples:**

- `improv: update gems`
- `fix: resolve DNS lookup problem`
- `feat: add FB OAuth sign in form`

**Bad examples:**

- `improv: coding`
- `fix: that was wrong`
- `test: write tests to check credentials for signed in and anonymous users`

## Long description (optional)

This is place where You can place your poetry. You can describe what you have done and why, give links to resources that you used, etc.

This is optional, so if you don't want, then you can leave this part empty. Have fun.

## Issues relationship (optional)

Is this commit related to some issue? Maybe it closes one? This is place where you can signal that.

Remember that GitHub allows to [close issue via commit message](https://help.github.com/articles/closing-issues-via-commit-messages/) so this can help us with issue management.

**Examples:**

- `Close #42`
- `Related #666`

## Work time (required)

How much do you spend working on this issue? Use [Toggl](tooling/toggl.md) to measure Your work time, this will help Us with measuring how much time we spent on each of pull-requests. Don't worry, it is only information for PM.