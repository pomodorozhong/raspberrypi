# Setup ssh key

## Steps for Windows 10

1. Run `powershell` and `Run as administrator`.
2. Type in `ssh-keygen`, and follow the instruction to generate the key.
   + If you didn't use the default path to store it, then change the path in the next step accordingly.
3. Modify the `path_to_the_key`, `username`, `hostname` to meet your setup.

```powershell
cat path_to_the_key | & 'C:\Program Files\Git\usr\bin\ssh.exe' username@hostname "mkdir ~/.ssh/ && touch ~/.ssh/authorized_keys && cat >> ~/.ssh/authorized_keys"
```

If you store the key in the default path, and you didn't change the `username` and the `hostname` for the Raspberry Pi, then your script should look like this:

```powershell
cat ~/.ssh/id_rsa.pub | & 'C:\Program Files\Git\usr\bin\ssh.exe' pi@raspberrypi.local "mkdir ~/.ssh/ && touch ~/.ssh/authorized_keys && cat >> ~/.ssh/authorized_keys"
```

4. Copy-paste the modified script into `powershell`, and run it. This will put the ssh key into Raspberry Pi, so you can use it to authenticate the ssh connection from now on.

## Reference

+ [How to Generate SSH Key in Windows 10](https://phoenixnap.com/kb/generate-ssh-key-windows-10)