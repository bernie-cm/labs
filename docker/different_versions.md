## How to run different versions of a Docker image

### Pulling first version `latest`
- From drop down select the most recent tag `latest`
- Use the command `docker pull postgres:latest` to select the version
- Check the correct image was downloaded using `docker image ls`

### Pulling second version `trixie`
- In this example, if you want the `trixie` tagged image then select that from the drop down menu
- Run the command `docker pull postgres:trixie` to select and pull the desired version.
- Check that you have two `postgres` images downloaded.

**Note**: If you don't add a tag name after the `:` the default is `latest`.