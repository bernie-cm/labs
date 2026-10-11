## How to run different versions of a Docker image

### Pulling first version `latest`
- From drop down select the most recent tag `latest`
<img width="1221" height="690" alt="image" src="https://github.com/user-attachments/assets/8409ef2d-af3f-4c31-9426-cdad42f3556a" />
- Use the command `docker pull postgres:latest` to select the version
<img width="679" height="160" alt="image" src="https://github.com/user-attachments/assets/d6222aef-20a1-4c0c-b7eb-267547ab8f39" />
- Check the correct image was downloaded using `docker image ls`
<img width="749" height="233" alt="image" src="https://github.com/user-attachments/assets/63a64583-01b6-4adb-9878-767fc198fe97" />


### Pulling second version `trixie`
- In this example, if you want the `trixie` tagged image then select that from the drop down menu
- Run the command `docker pull postgres:trixie` to select and pull the desired version.
- Check that you have two `postgres` images downloaded.

**Note**: If you don't add a tag name after the `:` the default is `latest`.
