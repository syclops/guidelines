# Git Commit Message Guidelines

This set of guidelines concerns commit messages in Git. There is already a
wealth of resources on this topic that can be found by a simple web search. Here
I will cover my own set of guidelines, which are largely derived from popular
guidelines on the Internet.

## General Guidelines

### Format

Each commit message should have the following format:

```
Type (scope): short summary of change

Write here a longer summary of the change. Be sure to describe in prose
what you have changed and why.
```

The change type should be capitalized and chosen from the possible types
described below. Capitalizing the change type makes it easier to grep for, as
nothing else in the change summary (except for proper nouns) is capitalized.

The scope is a one-word summary of the file or portion of the repository that
has changed. This restriction helps encourage me to make small, atomic commits
that don't touch many areas at once.

*Every* line should be a maximum of *72 characters*. There is only one exception
to this rule, and that is when you paste content from sources like error logs.
The subject line should be a maximum of *50 characters*, including the type and
scope. These line length restrictions ensure that the messages are readable,
easily digestible, and encourage you to distill the change down to its essence.

### Commit Types

For code, I use a set of commit messages types that are virtually identical to
widely-accepted types. They are as follows:

Type | Meaning
---- | -------
`Feat` | Add a new feature
`Fix` | Fix a bug
`Doc` | Add code documentation
`Perf` | Improve performance
`Test` | Test an aspect of the code
`Refactor` | Do not add a feature or fix a bug
`Style` | Do not change the semantic meaning of the code
`Chore` | Change the build process, auxiliary tools, or libraries

Though the above list works fine for code, sometimes I write papers in LaTeX and
track changes to the files using Git. Because the types of changes made to text
differ from those made to code, I use the following set of commit message types
for text:

Type | Meaning
---- | -------
`Cont` | Add new content
`Fix` | Fix problems with content
`Aux` | Change non-text files, such as figures
`Note` | Note aspects of the text without incorporating it into the text.
`Test` | Test an aspect of the code
`Reorg` | Reorganize existing content
`Style` | Do not change the semantic meaning of the text
`Chore` | Change compilation options or auxiliary tools
