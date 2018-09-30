# Data

The `data/` directory contains various files for tracking and submission of
student contributions to Hacktoberfest 2018/Release 0.2.

## people.json

An `Array` of GitHub usernames for students in DPS909 and OSD600
participating in Hacktoberfest.  This list is used to generate and
reference other data below.

*If your username is missing, or incorrect, please send a PR to fix it.*

## posts.json

An `Object` containing blog post URLs, or other "posts" (docs, videos, etc)
grouped by GitHub username.  As you write posts about your work, please
update this file with relevant links.  The format is as follows:

```json
"username": [
    "http://blog.com/first-blog-post",
    "http://blog.com/second-blog-post"
],
"username2": [
    "http://username2.blogspot.com/fixing-a-bug"
]
```

## issues.json

An `Object` containing info about GitHub Issues being worked on, or which
have been completed, grouped by GitHub username.  As you begin working on
bugs, please record the info here.  The format is as follows:

```js
"username": [
    {
        repo: "filerjs/filer",
        number: 123
    },
    {
        repo: "Microsoft/vscode",
        number: 1235,
        isComplete: true
    }
]
```

In the example above, `username` is working on two Issues:

1. https://github.com/filerjs/filer/issues/123
2. https://github.com/Microsoft/vscode/issues/1235

The `repo` is the portion of the GitHub URL that comes after `github.com`: `https://github.com/{owner}/{name}`.  The `number` is the Issue number.

When you are finished working on an Issue (it has been closed), add
the `isComplete: true` property and value.  If `isComplete` is not present,
it is assumed that the Issue is still on-going.

> NOTE: make sure you have left a comment in any Issue you want to work on, and have been given the go-ahead from the project to fix it before you add it to this file.

## pull-requests.json

An `Object` containing info about GitHub Pull Requests being worked on,
or which have been completed, grouped by GitHub username.  When you submit a
Pull Request, please record the info here.  The format is as follows:

```js
"username": [
    {
        repo: "filerjs/filer",
        number: 300
    },
    {
        repo: "Microsoft/vscode",
        number: 3200,
        isMerged: true
    }
]
```

In the example above, `username` is working on two Pull Requests:

1. https://github.com/filerjs/filer/pull/300
2. https://github.com/Microsoft/vscode/pull/3200

The `repo` is the portion of the GitHub URL that comes after `github.com`: `https://github.com/{owner}/{name}`.  The `number` is the Pull Request number.

When your Pull Request is merged (and only if it gets merged), add
the `isMerged: true` property and value.  If `isMerged` is not present,
it is assumed that the Pull Request is not merged (yet).

> NOTE: it's possible that a Pull Request will NOT get merged for one reason or another.  This is outside your control, and you should still record your Pull Requests here, even if they never get merged.