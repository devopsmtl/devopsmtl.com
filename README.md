# devopsmtl.com

## Overview

This repository contains the website content for the
[DevOps Montreal website](http://www.devopsmtl.com/).

All documentation is written in
[Markdown](http://daringfireball.net/projects/markdown/syntax). The website uses
the [Hugo](https://gohugo.io) website framework.

The [multilingual mode](https://gohugo.io/content/multilingual/) of Hugo is used
in order to support both English and French languages side-by-side.

## Development

### Prerequisites

* [Hugo](https://gohugo.io/overview/installing/) >= 0.17


### Adding a page
In the top directory of this repository, start the Hugo webserver:

```
hugo server
```

Add the menu entry for both languages on the _config.toml_ configuration file. The
`url` and `weight` attributes should stay identical:

```
[[languages.en.menu.main]]
url    = "/page/foo/"
name   = "Foo English"
weight = 0

[...]

[[languages.fr.menu.main]]
url    = "/page/foo/"
name   = "Foo French"
weight = 0
```

Create the page for each language in the proper subdirectory, here
`content/page/foo.en.md` and `content/page/foo.fr.md`:

```
---
title: "Foo"
date: "2016-10-26"
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

### Adding an event

Fork or clone the project

```
git clone --recursive https://github.com/devopsmtl/devopsmtl.com.git
```
Use `--recursive` to also clone hugo theme.


In the top directory of this repository, start the Hugo webserver:

```
hugo server
```

Create the page for each language in the proper subdirectory, here
`content/post/january-1970.en.md` and `content/page/january-1970.fr.md`:

```
---
title: "Foo"
description: "Monthly meetup"
date: "2016-10-26"
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

Local test url should look like `http://localhost:1313/devopsmtl.com/` 