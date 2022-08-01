# MetadataConverter

## How to use

1. Download latest [Release-Windows.zip](https://github.com/paimooon/MetadataConverter/releases) and unzip
1. Bring `global-metadata.dat` into the Release-Windows folder
1. Open Windows Terminal and type: `./metadata.exe decryptmeta global-metadata.dat output.bin`
1. Open `output.bin` via text editor (e.g. VSCode)
1. Get [dispatchKey.txt and passwordKey.txt](https://github.com/Grasscutters/Cultivation/tree/main/src-tauri/keys)
1. Find `<Modulus>~~~</Modulus>` of `output.bin`
1. Replace each key, dispatchKey is index 3 and passwordKey is 2.
1. Back to Windows Terminal and type: `./metadata.exe encryptmeta output.bin global-metadata-modified.dat`
1. Replace with the modified one
