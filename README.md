


## Installation

Requires Hugo > 0.42

    git submodule add https://gitlab.com/roneo.org/hugo-shortcode-roneo-button-icon-badge.git themes/hugo-shortcode-roneo-button-icon-badge

Edit `config.toml`

    theme = ["hugo-shortcode-roneo-button-icon-badge", "YourCurrentTheme"]

This adds this Shortcode as a "Theme component". See [the documentation](https://gohugo.io/hugo-modules/theme-components/)


### Call from a Markdown file

with the following Shortcode

```go
{{< button text="CSS" >}}
```

with an icon

```go
{{< button text="CSS" icon="css" >}}
```

### Call from a template


    {{ partial "button.html" (dict "context" . "pages" $.Site.Pages "text" "Hi there" "icon" "git") }}


### Add more icons

See `layouts/partials/svg/`


### Customize CSS

