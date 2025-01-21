## Dependencies

### libssh

https://github.com/apotocki/libssh2-iosx.git

- Using OpenSSL 1.1.1w

### OpenSSL

- Using Pod

```
pod 'OpenSSL-Universal', '1.1.2301'
```

## Updates and Fixes

### SSH Connection Issue Fix (Specific to iOS)
**Problem and Root Cause**

When attempting to establish an SSH connection using an iOS device, the connection may fail due to the older version of the libssh library not supporting the `ecdh-sha2-nistp256` algorithm for key exchange. The error message would be like this:

```
NMSSH: Socket connection to xxx.xxx.xx.xx on port 22 succesful
NMSSH: Failure establishing SSH session
```

**Solution**

To resolve this issue, I have updated the libssh library in this fork to a version that supports the `ecdh-sha2-nistp256` algorithm. Simply use this fork in your project to benefit from the fix:
```
pod 'NMSSH', :git => 'https://github.com/speam/NMSSH.git'
```
