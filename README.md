## Updates and Fixes

### SSH Connection Issue Fix (Specific to iOS)
**Problem Description**

When attempting to establish an SSH connection using an iOS device, you may encounter a failure in key exchange. Specifically, the connection fails when using the `ecdh-sha2-nistp256` algorithm for key exchange.

**Root Cause**

This issue arises due to the older version of the libssh library not supporting the `ecdh-sha2-nistp256` algorithm.
