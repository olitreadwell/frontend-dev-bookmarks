# What this revival changed

This fork runs the gate from
<https://github.com/olitreadwell/awesome-list-template>, over the index readme.

## The shape of this list

`README.md` is not the list. It is an index: fifty-six entries, each pointing at
one of the list's own category files, and those files hold several thousand
links. The gate reads one readme, so what it checks here is the index.

## The index

- The intro and the badges sat below the Contents block, which put the
  navigation before the thing it navigates. They are above it now.
- Every entry separated its link from its description with a colon, and wrapped
  the link in bold. Neither survives contact with the linter. The separator is
  ` - `, and the bold is gone.
- Every entry pointed at a relative path, which the linter reads as an invalid
  link and the engine reads as a URL with no scheme. Each one is now the
  absolute URL of the same file on GitHub.
- The awesome badge pointed at the dead rawgit CDN. It points at awesome.re.
- `# License` was an h1 and the linter forbids a licence section in the readme.
  The licence is a `LICENSE` file now, with the CC BY 4.0 legal code, and the
  readme section is gone.
- Thematic rules ran to eighty dashes. They are three.
- Six entries described themselves by repeating their own name.
- `github.stats` is off in `awesome.toml`. Every entry points at a file inside
  one repository, so a stars and last-push line would have been the same number
  on all fifty-six lines. Turn it back on the moment an entry links a real
  repository.

## What is left

The category files are not checked and not audited:

```
appearance/ architecture/ compatibility/ ecosystem/
languages-protocols-browser-apis/ user-interface-components/ workflow/
TOTALLY-GIGANTIC-FILE.md
```

They hold 4,317 lines of links collected up to 2015, and most of them are dead.
Auditing that is a separate job with its own budget. `make links` runs lychee
over the readme the config points at, so the tooling is there when that job
starts, but nothing in this fork claims those files are current.

Nothing in this commit writes a description. The words are upstream's.
