# Deephaven Contributor License Agreement (CLA)

![Deephaven Data Labs Logo](docs/images/Deephaven_GH_Logo.svg)

This repository contains the Deephaven Contributor License Agreement (CLA) as well as a record of CLA signaures.  Signatures can be found in [./signatures/](./signatures/).

There is a GitHub Action to manage Contributor License Agreement (CLA) compliance.  This action uses CLA Assistant (https://github.com/marketplace/actions/cla-assistant-lite) to ensure that all contributors have signed the Deephaven CLA before their PRs are merged.  The CLA can be signed by commenting on a PR.  

To enable the GitHub Action to manage Deephaven CLA compliance:

1. Add the GitHub Action to your project.

    ```bash
    cd <your_project>
    mkdir -p .github/workflows/
    curl https://raw.githubusercontent.com/deephaven/cla/main/actions/cla.yml > .github/workflows/cla.yml
    ```

2. Set `PERSONAL_ACCESS_TOKEN`

    A personal access token must be set up to allow this bot to commit to the CLA repository.  To do this:
    a) Create a personal access token with repo scope
    b) Manually add the token to your repository's secrets as `PERSONAL_ACCESS_TOKEN`

3. Edit the `allowlist`

    If a GitHub username is included in the `allowlist`, they will not be required to sign the CLA.  This is useful for allowing bots to contribute without a CLA.  The `allowlist` can be set in the GitHub Action (`cla.yml`).

**The main branch of this repository must not be protected.**

