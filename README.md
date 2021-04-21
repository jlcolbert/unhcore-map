# UNHCore Metadata Application Profile

## Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Code of Conduct](./CODE_OF_CONDUCT.md)

## About <a name = "about"></a>

UNHCore is the property set for the University of New Hampshire Library's Digital Collections. The UNHCore Metadata Application Profile (MAP) gives the general guidelines, standards, best practices, and description of the property set.
UNH Digital Collections are currently hosted in Digital Commons; the unique considerations for that system are are represented in this MAP. Because Digital Commons is a temporary host for the collections, the standards will change when we eventually migrate systems.
This repository contains the MAP in Markdown files, as well as PDF and Word. The MAP is also represented in [Wiki](https://github.com/jlcolbert/unhcore-map/wiki) form.

## Getting Started <a name = "getting_started"></a>

This MAP can be used without setting up on a local machine; simply reference the Wiki or the documents within the repository.
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

1. An editor for Markdown files, specifically GitHub Markdown
2. A GitHub account if you plan to submit issues
3. Git and a GitHub account if you plan to clone/form this repository, make edits, and submit pull requests
4. HubFlow, if you want the branch workflow automated
5. Yarn, if you plan on using the CLI linters/formatters

### Installing

1. Clone this repository on your local machine

```sh
git clone https://github.com/jlcolbert/unhcore-map.git # https://github.com/jlcolbert/unhcore-map.wiki.git for Wiki files
cd unhcore-map
```

2. Create a feature branch for your contribution(s)

```sh
# Using git
git branch feature/<YOUR NAME OR FEATURE>
```

```sh
# Using HubFlow
cd
git clone https://github.com/datasift/gitflow
cd gitflow
sudo ./install.sh
cd <PATH BACK TO UNHCORE-MAP>
git hh init
git hf feature start <YOUR NAME OR FEATURE>
```

### Making Changes

1. Follow the [Arctic Ice Studio Markdown Style Guide](https://github.com/arcticicestudio/styleguide-markdown) for Markdown style best practices; this repository already has the linters/formatters and their configurations installed. (You will need to look up how to use linters and formatters in the command line or in your editor.)
2. Commit early and often. Use the [Arctic Ice Studio Git Style Guide](https://github.com/arcticicestudio/styleguide-git) for git best practices.
3. When you're done with your changes and committed them, you can create a pull request off the "develop" branch for your feature branch.

## Usage <a name = "usage"></a>

This MAP is meant for the Digital Collections at the University of New Hampshire. It is meant to be guidelines rather than strict rules, as there will always be exceptions. *The most important thing is to be consistent.*
