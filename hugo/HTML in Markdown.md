Add a shortcode template to your site, in layouts/shortcodes/rawhtml.html, with the content:

```
<!-- raw html -->
{{.Inner}}
```

You can then use this shortcode in your markdown content, like so:

```
{{< rawhtml >}}
  <p class="speshal-fancy-custom">
    This is <strong>raw HTML</strong>, inside Markdown.
  </p>
{{< /rawhtml >}}
```

[Source](https://anaulin.org/blog/hugo-raw-html-shortcode/)
