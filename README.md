This is a simple Obsidian starter.

# Get started

There are various ways to use this starter. But I recommend using "lindir" to centralize your Obsidian configuration(+ plugins) with this starter.

By following below steps, you'll create your centralized Obsidian configuration repository.

## 1. Create a repository with this template

First, create a repository with this template. You can click a button "Use this template" or visit URL below to create your repository.

[Use this template](https://github.com/new?template_name=obsidian-starter&template_owner=Galacsh)

## 2. Clone your repository

```shell
git clone <your-repository>
```

## 3. Open in Obsidian

Open your repository as a vault in Obsidian and make some tweaks.

## 4. Initialize Lindir

> [!WARNING]
> You need [Lindir](https://github.com/Galacsh/lindir) to synchronize your configuration between multiple vaults.

```shell
cd <your-repository>
lindir init
```

Since this repository already has `.lindirignore`, for most of the case, you don't need to take care of ignoring files.

## 5. Link to a new vault

Use Lindir to connect your Obsidian configuration repository to a new vault.

```shell
lindir link <your-new-vault>
lindir link <another-new-vault>
```

## 6. Push changes to linked vaults

You can push changes(new files, deleted files) to the linked vaults by:

```shell
lindir push
```

If changes are scattered in linked directories, you can sync them by:

```shell
lindir sync
```

## 7. Custom File Explorer sorting plugin

To sort files in file explorer, you need to create `config/sort.md`.

> [!TIP]
> Plugin repository: [Custom File Explorer sorting](https://github.com/SebastianMC/obsidian-custom-sort).

This is an example of `config/sort`:

```markdown
---
sorting-spec: |-
  target-folder: /
  README
  Quick Notes
  Projects
  %
  config
  order-asc: a-z

  target-folder: Quick Notes
  target-folder: Projects
  order-desc: created
---
```

## 8. Iconize plugin

Should manually configure `iconize` plugin.

Example configuration:

```json
{
  "settings": {
    "migrated": 3,
    "iconPacksPath": ".obsidian/icons",
    "fontSize": 14,
    "emojiStyle": "native",
    "iconColor": null,
    "recentlyUsedIcons": [],
    "recentlyUsedIconsSize": 10,
    "rules": [],
    "extraMargin": {
      "top": 0,
      "right": 4,
      "bottom": 0,
      "left": 0
    },
    "iconInTabsEnabled": true,
    "iconInTitleEnabled": false,
    "iconInFrontmatterEnabled": false,
    "iconsBackgroundCheckEnabled": false,
    "iconsInNotesEnabled": true
  }
}
```
