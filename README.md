# OpenAttestationMerkleProofSignature2018

This specification defines the proof format for use with [OpenAttestation V3 Verifiable Credentials](https://www.openattestation.com/docs/docs-section/roadmap/v3/overview).

**Read the draft**: <https://Open-Attestation.github.io/OAMerkleProofSignature2018>

# Repo notes:
This repo is dependant on [poetry](https://python-poetry.org/) dependency management for its python packages. 

Please do install poetry in order to run the generator locally if you would like to preview the ReSpec document locally.

Alternatively, one could also upload the `.bs` (bikeshed) file onto this [site](https://api.csswg.org/bikeshed/) as an escape hatch if one doesn't want to bother dealing with setting up the repository.

# Getting Started:

First install all the dependencies required
```shell
poetry install
```

The workflow is as follows: do edits on the bikeshed file (bikeshed is w3c's variant on the markdown spec), then generate the spec file using these commands.

## Generating, watching and serving the spec
```shell
poetry run task dev
```

This command will generate the spec file, watch for any edits and serves the generated spec file on port `8000` (for non technical users, this means visiting [here](http://localhost:8000)). There is a need to refresh the page eveytime you make an edit.

## Generating the spec
```shell
poetry run task gen
```

This command just generates the spec file, which should be named `index.html` (normally you will not use this).

# Publishing the spec on github-pages:

This repo has been configured with a github action that depends on a premade workflow by the w3c committee. 

Once a pull request is merged, the spec will be automatically published on github-pages.