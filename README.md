

## Objective

This Hugo Theme Component allows to easily **insert Badges and Buttons in your content and templates**

Both a [Shortcode](https://gohugo.io/content-management/shortcodes/) and a [Partial Template](https://gohugo.io/templates/partials/) are provided.

## Screenshot

![Insert buttons and badges with an optional icon](https://roneo.org/illustrations/hugo-shortcode-roneo-button-icon-badge/hugo-shortcode-roneo-button-icon-badge-screenshot.jpg)

## Usage

```
{{< badge text="CSS" icon="css" >}}
```

## Options

```
text= "string" # REQUIRED
icon= "SVG icon name"
href= "URL"
id= "string"
class= "custom-class"
```

Only the `text` parameter is required.

The `icon` parameter must match one of the filenames at `/layouts/partials/svg/`.  
You can add more files by creating the same directory structure in project root.


## Installation

(Requires Hugo > 0.42)

Install as a Git submodule:

    git submodule add https://gitlab.com/roneo.org/hugo-shortcode-roneo-button-icon-badge.git themes/hugo-shortcode-roneo-button-icon-badge

Edit `config.toml`:

    theme = ["hugo-shortcode-roneo-button-icon-badge", "YourCurrentTheme"]
    enableInlineShortcodes = true

To learn more about "Theme components", see [the Hugo documentation](https://gohugo.io/hugo-modules/theme-components/)


### Insert in a Markdown file

with the following Shortcode:

```go
{{< badge text="CSS" >}}
```

Insert a badge with an icon:

```go
{{< badge text="CSS" icon="css" >}}
```

### Call from a template

```go
{{ partial "badge.html" (dict "context" . "pages" $.Site.Pages "text" "Hi there" "icon" "git") }}
```

### Add more icons

Add SVG files in `/assets/svg/`.  
You can edit the Component directory or create the same folder structure at the root of your project.

Note that some SVG files do not work (#TODO:investigate), see `/assets/svg/` to get inspiration.


## Contribute

Please star this repo [on Github](https://github.com/RoneoOrg/hugo-shortcode-roneo-button-icon-badge) or [Gitlab](https://gitlab.com/Roneo/hugo-shortcode-roneo-button-icon-badge), to help this project gain some visibility and reach new contributors.

Code contributions are welcome, and the main place for development is [this Gitlab repo](https://gitlab.com/Roneo/hugo-shortcode-roneo-button-icon-badge). Feel free to use [this Github repo](https://github.com/RoneoOrg/hugo-shortcode-roneo-button-icon-badge).

## References

- Inspired by the [Button Shortcode](https://github.com/marketempower/axiom/blob/master/layouts/shortcodes/button.html) from the [Axiom Theme](https://www.axiomtheme.com/docs/shortcodes/#button)
- [Hugo documentation about Theme Components](https://gohugo.io/hugo-modules/theme-components/)
- Hugo documentation about [Shortcodes](https://gohugo.io/content-management/shortcodes/)
- Hugo documentation about [Partial Templates](https://gohugo.io/templates/partials/).