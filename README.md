# upload-image-action
GitHub action for saving Docker image in run's artifacts

Workflow with the action usage example:

```
name: Release Image

jobs:
  test:
    steps:
    - name: Checkout commit
      uses: neuro-inc/upload-image-action@v21.9.3
      with:
        image: platformstorageapi
        token: ${{ secrets.GITHUB_TOKEN }}
```


Arguments:

`image` -- the image name without tag, e.g. `platformstorageapi`.
`token` -- secret github token, pass: `${{ secrets.GITHUB_TOKEN }}` or generated Personal Access Token.
`artifact` -- uploaded artifact name, `image` by default.  Use https://github.com/neuro-inc/release-image-action` to release previously uploaded artifact on ghcr.io
