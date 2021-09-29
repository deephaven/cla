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
    git add .github/workflows/cla.yml
    ```

2. Edit the `allowlist`

    If a GitHub username is included in the `allowlist`, they will not be required to sign the CLA.  This is useful for allowing bots to contribute without a CLA.  The `allowlist` can be set in the GitHub Action (`cla.yml`).

3. Request access for your repo to `CLA_PERSONAL_ACCESS_TOKEN`

    The action requires access to the `CLA_PERSONAL_ACCESS_TOKEN` organizational secret.  You must request access to this secret for your repository.  If the repository does not have access to the secret, the action will fail with an error that looks like:

    ```
    Error: Parameter token or opts.auth is required
    ```

**The main branch of this repository must not be protected.**

