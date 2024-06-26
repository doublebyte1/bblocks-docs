---
title: Setting up imports
permalink: /create/imports
---
Any building blocks repository can import any other repository, so that references by id to building blocks
(e.g. inside schemas, in `bblock.json`, etc.) belonging to the imported repositories can be automatically resolved.

Repository imports can be defined as an array of URLs to the output `register.json` of other repositories inside
`bblocks-config.yaml`:

* If `imports` is missing from `bblocks-config.yaml`, the
  [main OGC Building Blocks repository](http://blocks.ogc.org/register.html) will be imported by default.
* `default` can be used instead of a URL to refer to the
  [main OGC Building Blocks repository](http://blocks.ogc.org/register.html). 
* If `imports` is an empty array, no repositories will be imported.

For example, the following will import two repositories, one of them being the main OGC Building Blocks repository:

```yaml
name: Repository with imports
imports:
  - default
  - https://example.com/bbr/repository.json
```