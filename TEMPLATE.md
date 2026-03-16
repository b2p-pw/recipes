#### App `metadata.json`

``` json
{
  "metadata_version": 1,
  "package": "my-app",
  "target": "b2p",
  "display_name": "My App!",
  "description": "My cool app can do awesome things.",
  "tags": ["cli", "app", "cool"],
  "categories": ["entertainment"],
  "authors": ["App author", "App author team"],
  "maintainers": ["My self", "My team"],
  "license": "MIT",
  "homepage": "https://my-app-homepage.cool",
  "repository": "https://github.com/app-team/my-app",
  "default": {
    "recipe_version": "1.0.0",
    "flavor": "vanilla"
  }
}
```

#### Lib `metadata.json`

``` json
{
  "metadata_version": 1,
  "package": "my-lib",
  "target": "l2p",
  "display_name": "My Lib!",
  "description": "My cool lib can do awesome things.",
  "tags": ["cli", "lib", "cool"],
  "categories": ["utilities", "development"],
  "authors": ["Lib author", "Lib author team"],
  "maintainers": ["My self", "My team"],
  "license": "MIT",
  "homepage": "https://my-lib-homepage.cool",
  "repository": "https://github.com/lib-team/my-lib",
  "default": {
    "recipe_version": "1.0.0",
    "flavor": "vanilla"
  }
}
```

#### App `manifest.json`

``` json
{
  "manifest_version": 1,
  "b2p_requirement": ">=1.0.0",
  "package": "my-app",
  "recipe_version": "1.0.0",
  "flavor": "vanilla",
  "environment": {
    "kernel": "Windows NT",
    "depends": {
      "net@runtime": ">=7.15"
    }
  },
  "runtime": {
    "shims": [
      {
        "name": "bin-1",
        "binary": "bin/binary 1.exe",
        "args": "--path 'C:\\'"
      },
      {
        "name": "bin-2",
        "binary": "bin/binary 2.exe"
      }
    ],
    "backup": {
      "files": [
        "config.ini",
        "data/data.json"
      ]
    }
  },
  "scripts": {
    "installer": "recipe.yaml",
    "remover": "remove-directory"
  }
}
```

#### `checksums.sha256`

``` sha256
a1b2c3d4e5f6...  manifest.json
b8d9c0e1f2a3...  recipe.yaml
```

#### `label.md`

``` md
# My App

> A short, punchy tagline that describes the flavor of this software.

## ✨ Highlights

- **Key Feature 1:** Why is this app special?
- **Key Feature 2:** What problem does it solve?
- **Key Feature 3:** Why download the `b2p` version?

## 🚀 Quick Taste

Example command to show the app in action:

    my-app --help

## 📝 About

A more detailed description of the ingredients and what the user can expect after the installation.
```