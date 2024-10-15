# Obsidian CMS

This is a demo of a CMS built with [Obsidian](https://obsidian.md/).

The idea is to use Obsidian as a CMS for a static site generator. This repository contains a sample vault with a few notes and templates to get you started.

> Note: This is a WIP, and the instructions for pulling the content from Obsidian into a static site generator are not yet complete. A `bash` script could be used on the destination machine to pull the content from the Obsidian vault and generate the static site.

## Requirements

- [Obsidian](https://obsidian.md/) installed on your machine

## Installation

1. Clone this repository to your local machine
2. Open Obsidian, and click on the 'Open Vault' button
3. Navigate to the folder where you cloned this repository, and select it
4. Select 'Trust Author and Enable Plugins' when prompted (you can also open the vault in Restricted Mode and enable the plugins manually... but that's no fun)

## Usage

Instructions for using or extending Obsidian can be found at on their Documentation site: [Obsidian Developer Docs](https://docs.obsidian.md/)

---
## Obsidian CMS Features

### CSS Snippets

The vault comes with a few CSS snippets to style the editor and the preview pane. You can find these snippets in the `.obsidian/snippets` folder. These snippets are applied to the vault by default. You can turn these on or off in the Obsidian settings, or modify them in the `.obsidian/appearance.json` file.

### Plugins

#### Git

[Vinzent03/obsidian-git](https://github.com/Vinzent03/obsidian-git)

This plugin allows you to sync your vault with a git repository. This is useful for version control and collaboration.

#### Hider

[kepano/obsidian-hider](https://github.com/kepano/obsidian-hider)

This plugin allows you to hide certain elements in the editor, such as the frontmatter, or the preview pane. This is useful for keeping the editor clean and focused.

#### Templater

[SilentVoid13/Templater](https://github.com/SilentVoid13/Templater)

This plugin allows you to create templates for your notes. The vault comes with a few templates to get you started (located in the `_utils/templates` folder).
