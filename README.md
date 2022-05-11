# artifactory-get-latest-image-tag
Get the latest tag from Artifactory for an Docker image


## Usage: 

``` yaml
  uses: asml-actions/artifactory-get-latest-image-tag@setup
  id: get-tag
  with:
    ARTIFACTORY_URL: https://my_artifactory_server.com
    REPO_KEY: reg-local
    IMAGE_NAME: runner
    ARTIFACTORY_TOKEN: ${{ secrets.ARTIFACTORY_TOKEN }}

  -name: Show the tag from the output of the previous step  
   env: 
     TAG: 
   run: echo "Found this tag:: [${{ steps.get-tag.outputs.tag }}]"
```