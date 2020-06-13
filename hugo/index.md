# Not rendering HTML in Markdown:

Paste this is config.toml
```
[markup]
  defaultMarkdownHandler = "goldmark"
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true
```
