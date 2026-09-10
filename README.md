# INTELSYS schemas

Published JSON Schemas for INTELSYS file formats, served at
**https://schemas.intelsys.ca/**.

This repository is public for one reason: a `$schema` URL only works if anybody
can fetch it. Editors such as Visual Studio Code and Visual Studio download it
to offer completion and validation while somebody edits the file.

## Install Studio project files (`.isproj`)

```
https://schemas.intelsys.ca/install-studio/isproj-v17.schema.json
```

An `.isproj` is the declarative description of an installer, and is the contract
between the INTELSYS Install Studio designer, the `isbuild` command line, and
the packagers. Anything the designer can produce is reproducible from this file
alone.

Every version ever published stays here, at its own address, forever. Older
projects still open and still build, because every field added since is
optional — and a URL written into somebody's project file five years ago must
not stop resolving.

| Version | Address |
|---|---|
| 17 (current) | `install-studio/isproj-v17.schema.json` |
| 1 – 16 | `install-studio/isproj-v<n>.schema.json` |

## Where these come from

They are maintained in the Install Studio repository and copied here. Do not
edit them in this repository — a change made here would be overwritten and, more
importantly, would no longer match the product that reads the files.

The Install Studio build checks that every schema names its own version, and
that the version the product writes into new projects is one that exists here.
