`metadata.json`

``` json
{
    "package": "my-app",
    "description": "My cool app can do awesome things.",
    "author": ["App author", "App author team"],
    "maintainers": ["My self", "My team"],
    "license": "Unlicense",
    "homepage": "https://my-app-homepage.cool",
    "repository": "https://github.com/app-team/my-app",
    "default": {
        "version": "1.0.0",
        "flavor": "vanilla"
    },
    "tags": ["cli", "app", "cool"],
    "categories": ["Utilities", "Development"]
}
```

`manifest.json`

``` json
{
    "package": "my-app",
    "version": "1.0.0",
    "flavor": "vanilla",
    "environment": {
        "kernel": "Windows NT",
        "depends": {
            "net": ">=7.15"
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

`checksums.sha256`

``` sha256
a1b2c3d4e5f6...  manifest.json
b8d9c0e1f2a3...  recipe.yaml
```