# MetadataConverter

## How to use

1. Download latest [Release-Windows.zip](https://github.com/paimooon/MetadataConverter/releases) and unzip
1. Bring `global-metadata.dat` into the Release-Windows folder
1. Open Windows Terminal and type: `./metadata.exe decryptmeta global-metadata.dat output.bin`
1. Open `output.bin` via text editor (e.g. VSCode)
1. Get [SigningKey.pem](https://github.com/Grasscutters/Grasscutter/blob/development/src/main/resources/keys/SigningKey.pem) and [convert to xml](https://the-x.cn/en-US/certificate/PemToXml.aspx)
1. Find `<Modulus>~~~</Modulus>` of `output.bin` and replace with the xml converted one
1. Back to Windows Terminal and type: `./metadata.exe encryptmeta output.bin global-metadata-modified.dat`
1. Replace with the modified one
