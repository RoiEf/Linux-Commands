1. Acquire build files from Arch Linux user repository.
```
curl -L -O https://aur.archlinux.org/cgit/aur.git/snapshot/visual-studio-code-bin.tar.gz
```
2. Extract the downloaded package
```
tar -xvf visual-studio-code-bin.tar.gz
```
3. Change directory to the extracted package
```
cd visual-studio-code-bin
```
4. Build and install the package
```
makepkg -si
```