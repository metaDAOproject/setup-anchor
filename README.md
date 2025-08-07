# Setup Anchor

An optimized action for installing [Anchor](https://www.anchor-lang.com/).

If you just need Solana (without Anchor), you should also check out [Setup Solana](https://github.com/metaDAOproject/setup-solana).

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
      - uses: metadaoproject/setup-anchor@v3.3
      - run: anchor build
        shell: bash
```

This will use the default versions of Anchor, Node.js, and the Solana CLI tools, which are 0.31.1, 20.11.0, and 2.2.21 respectively. You can also configure these versions like so:

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: metadaoproject/setup-anchor@v3.1
    with:
      anchor-version: '0.30.1'
      solana-cli-version: '1.18.18' # Set it to 2.x.x to use the Anza release
      node-version: '20.16.0'
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
