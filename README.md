# scripts
1. The first step into adding scripts to Files is to create the directory where it expects your scripts to be. If it doesn’t exist already, create the following directory:

```
mkdir -p ~/.local/share/nautilus/scripts/
```
2. Create script 
```
vim ~/.local/share/nautilus/scripts/convert_to_jpeg
echo -e "$NAUTILUS_SCRIPT_SELECTED_FILE_PATHS" | xargs -i convert "{}" "{}.jpg"
```
3. Make the script executable
```
chmod +x ~/.local/share/nautilus/scripts/convert_to_jpeg
```
