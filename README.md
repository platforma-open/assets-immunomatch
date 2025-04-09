# ImmunoMatch Model Assets

This repository wraps the following ImmunoMatch models:
- [ImmunoMatch Kappa at commit 0721a61](https://huggingface.co/fraternalilab/immunomatch-kappa/commit/0721a611a29980efb061780833da8fe7eebec1e4)
- [ImmunoMatch Lambda at commit a01c38e](https://huggingface.co/fraternalilab/immunomatch-lambda/commit/a01c38e17450acebce2d8bcc2226c25cd2b029db)

## Attributions

### Appropriate credit

1. Name of the creator: [fraternalilab](https://fraternalilab.github.io/)
2. No changes were made to the models.

### Link to the license

Both models are licensed under [cc-by-nc-4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.en):
- https://huggingface.co/fraternalilab/immunomatch-kappa/resolve/0721a611a29980efb061780833da8fe7eebec1e4/README.md
- https://huggingface.co/fraternalilab/immunomatch-lambda/resolve/a01c38e17450acebce2d8bcc2226c25cd2b029db/README.md


## Structure

- immunomatch-kappa/: [Kappa model](https://huggingface.co/fraternalilab/immunomatch-kappa)
- immunomatch-lambda/: [Lambda model](https://huggingface.co/fraternalilab/immunomatch-lambda)
- catalogue/: Catalogue of all available models

## Usage

Each model directory contains:
- package.json: Package configuration
- modelFileUrls.json: Model file URLs and metadata

## How to update the models to newer versions

### Gather upstream updated information

1. Go to the huggingface repository that is being updated and get the latest commit ID. For example [immunomatch-kappa]https://huggingface.co/fraternalilab/immunomatch-kappa/tree/main).
2. Copy the commit ID to be synced to. It will be used in the next section.
3. Take note of the filenames. You will need to double-check them in the next section against the `model_files`.

### Update projects with the gathered information

1. Go to the model folder (i.e. `immunomatch-kappa`), and find the `modelFileUrls.json` file.
2. Update the `model_url` to point to the commit id you are upgrading to.
    ```
    "model_url": "https://huggingface.co/fraternalilab/immunomatch-kappa/resolve/<new-commit-id-goes-here>",
    ```
3. Ensure `model_files` contains the same file names as in the upstream huggingface model.
4. Update this README.md file with the new <commit-id>
    - All URLs using the old commit ID must be updated to use the new commit ID
    - If the license has changed, the [## Attributions](#attributions) section must be updated too.
