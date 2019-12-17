# Blackburn

Blackburn is a clear and responsive theme for [Hugo](//gohugo.io), by [Yoshiharu Yamashita](https://github.com/yoshiharuyamashita/blackburn).
Blackburn-mod is a light modification of Blackburn to disintermediate fonts, css, and javascript in order to reduce users' exposure
to the global surveillance apparatus.

Some of the below Readme no longer applies, I have tried to keep this update where relevant.

## Overview

* Based on Yahoo's [Pure CSS](http://purecss.io/) (v1.0.0)
* Fixed sidebar with social links:
  * GNU social
  * Flickr
  * Pinterest
  * Vimeo
  * Reddit
  * Hacker News
  * GitHub
  * GitLab
  * Bitbucket
  * Stack Overflow
  * Server Fault
  * Steam
  * MobyGames
  * Last.fm
  * Discogs
  * Keybase
* Client-side syntax highlighting by [Highlight.js](//highlightjs.org) (v9.12.0)
* Icons by Fork Awesome

## Screenshots

![screenshot](https://raw.githubusercontent.com/yoshiharuyamashita/blackburn/master/images/screenshot.png)

## Installation

In your Hugo site directory, run:

```shell
$ mkdir themes
$ cd themes
$ git clone https://github.com/yoshiharuyamashita/blackburn.git
```

or download from [here](//github.com/yoshiharuyamashita/blackburn/archive/master.zip).

See [Hugo Quickstart Guide](//gohugo.io/overview/quickstart/) for more information.

## Configuration

Example config.toml:

```toml
baseurl = "https://www.example.com/" # Make sure to end baseurl with a '/'
title = "Your site title"
author = "Your name"
# Shown in the side menu
copyright = "&copy; 2016. All rights reserved. Licensed under the Creative Commons BY-SA License, Version 3 or Later"
canonifyurls = true
paginate = 10

[indexes]
  tag = "tags"
  topic = "topics"

[params]
  # Shown in the home page
  subtitle = "A Hugo Theme"
  brand = "Blackburn"
  # CSS name for highlight.js
  highlightjs = "androidstudio"
  highlightjs_extra_languages = ["yaml"]
  dateFormat = "02 Jan 2006, 15:04"
  # Include any custom CSS and/or JS files
  # (relative to /static folder)
  custom_css = ["css/my.css"]
  custom_js = ["js/my.js"]


[menu]
  # Shown in the side menu.
  [[menu.main]]
    name = "Home"
    pre = "<i class='fa fa-home fa-fw'></i>"
    weight = 1
    identifier = "home"
    url = "/"
  [[menu.main]]
    name = "Posts"
    pre = "<i class='fa fa-list fa-fw'></i>"
    weight = 2
    identifier = "post"
    url = "/post/"
  [[menu.main]]
    name = "About"
    pre = "<i class='fa fa-user fa-fw'></i>"
    weight = 3
    identifier = "about"
    url = "/about/"
  [[menu.main]]
    name = "Contact"
    pre = "<i class='fa fa-phone fa-fw'></i>"
    weight = 4
    url = "/contact/"

[social]
  # Link your social networking accounts to the side menu
  # by entering your username or ID.

  # SNS microblogging
  gnusocial = "*" # Specify full href (e.g. https://quitter.se/yourusername)
  mastodon = "*"

  # SNS photo/video sharing
  pixelfed = "*" # Specify full href
  flickr = "*"
  photo500px = "*"
  pinterest = "*"
  vimeo = "*"
  slideshare = "*"

  # SNS news
  reddit = "*"
  hackernews = "*"

  # Techie
  github = "yoshiharuyamashita"
  gitlab = "*"
  bitbucket = "*"
  stackoverflow = "*"

```

## Usage

* Write Markdown files in `content/post`
* Add fixed pages (e.g., about.md) to the side menu by defining them under `[menu]` in the config.toml:

```toml
[[menu.main]]
  name = "About"
  pre = "<i class='fa fa-user fa-fw'></i>"
  weight = 2
  identifier = "about"
  url = "/about/"
```

* Override the theme by linking to custom CSS files:

```toml
[params]
  custom_css = ["css/my.css"]
```

* Add new behaviours by linking to custom JS files:

```toml
[params]
  custom_js = ["js/my.js"]
```

## Shortcodes

### pure_table
```
{{< pure_table
  "columnName1|columnName2|...|columnName99"
  "dataValue1|dataValue2|...|dataValue99"
  "dataValue1|dataValue2|...|dataValue99"
  "dataValue1|dataValue2|...|dataValue99"
  "... and so on"
>}}
```

where each positional parameter is separated by the vertical bar (i.e., |). The resulting `<table>` is set to have `class="pure-table pure-table-striped"`.

### fluid_imgs

```
{{< fluid_imgs
  "class|src|alt"
  "class|src|alt"
  "... and so on"
>}}
```

where each positional parameter is separated by the vertical bar (i.e., |).

- `class`: specifies a Pure CSS unit class name (**required**)
- `src`: specifies the URL of an image (**required**)
- `alt`: specifies an alternate text for an image (optional)

See [here](http://yoshiharuyamashita.com/post/hugo-shortcode-to-show-multiple-images/) for examples.

### fluid_img (obsolete)

#### Positional

```
{{% fluid_img "/path/to/img" %}}
```

#### Named

```
{{% fluid_img class="pure-u-1-2" src="/path/to/img" alt="img description" %}}
{{% fluid_img class="pure-u-1-3" src="/path/to/img" caption="img description" %}}
```

* `class`, `alt` and `caption` are optional.
* See [Pure CSS Grids](http://purecss.io/grids/) for possible `class` values.

## License

* [MIT](//opensource.org/licenses/MIT)

