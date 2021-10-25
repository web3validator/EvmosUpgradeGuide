# This guide about to upgrade evmosd binary

1. Create folder where we will download all necessary files:
```bash
mkdir $HOME/evmos_temp && cd $HOME/evmos_temp 
```
![image](https://user-images.githubusercontent.com/59205554/138677097-c0db97c1-d7fa-4514-aedf-533e791eed18.png)

2. Download new version from the evmos git repository in releases:

```bash
wget https://github.com/tharsis/evmos/releases/download/v0.1.3/evmos_0.1.3_Linux_x86_64.tar.gz
```
![image](https://user-images.githubusercontent.com/59205554/138677183-bf0a8454-9222-41b7-b99e-0ebd6453180f.png)

3.  Unpack the archive with a simple command

```bash
tar -xzf evmos_0.1.3_Linux_x86_64.tar.gz
```
![image](https://user-images.githubusercontent.com/59205554/138677243-724eeb56-7049-4f3a-b414-1e22c7c95700.png)

4. Move new binary to the appropriate directory and check the version (it should be 0.1.3)

```bash
mv ./bin/evmosd $(which evmosd)
evmosd version
```
![image](https://user-images.githubusercontent.com/59205554/138678995-9ec1b655-8f23-45ab-ab4e-06b2568440fb.png)

5. Than we need too restart the service:

```bash
systemctl restart evmosd
```
![image](https://user-images.githubusercontent.com/59205554/138679110-58a86215-4637-4830-be14-d926a38c450e.png)

6. Сheck the logs to calm the soul:

```bash
journalctl -u evmosd -f 
```
![image](https://user-images.githubusercontent.com/59205554/138679169-21560f40-dd02-4ddb-98c5-f27d515ff992.png)

Enjoy it! Feel free to ask any question https://t.me/HeKit 
