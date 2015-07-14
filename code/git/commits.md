# Commit naming

In Nukomeet we use very strict commit naming convention that help us with further reviewing `git log`.

## Template

Template that we use looks like:

```raw
<commit type>: <short description>

<further, longer description>

<issues relationship> [<work time>]
```

Don't worry if it looks complicated. Only some of this fields are required and it is very easy to get used to.

### Commit types

To allow us to extract what was type of commit we begins our commit messages with commit type tag. There are a few of them:

| Name     | Description | Example |
| -------- | ----------- | ------- |
| `improv` | Refactoring and code style improvements | 2:2 |
| `feat`   | New features
| `fix`     | Code fixes |
| `docs`   |
| `style`  |
| `test`   |