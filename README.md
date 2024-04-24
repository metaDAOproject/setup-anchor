# Setup Anchor

An optimized action for installing [Anchor](https://www.anchor-lang.com/).

# Usage

Here's an example workflow:

```yaml
name: example-workflow
on: [push]
jobs:
  run-anchor-build:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v3
      - uses: metadaoproject/setup-anchor@v1.2
      - run: anchor build
        shell: bash
```

This will use the default versions of Anchor, Node.js, and the Solana CLI tools, which are 0.27.0, 16.15.1, and 1.15.2 respectively. You can also configure these versions like so:

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: metadaoproject/setup-anchor@v2
    with: 
      anchor-version: '0.28.0' 
      solana-cli-version: '1.14.20'
      node-version: '16.15.1'
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
