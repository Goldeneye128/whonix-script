# Whonix Build Script for Apple Silicon Macs

This script simplifies the process of building Whonix on Mac computers with Apple Silicon, enabling users to easily build Whonix on a Debian 12 virtual machine (VM).

## Installation and Usage Instructions

### Prerequisites

- Ensure you have a Debian 12 VM set up on your system. The VM should have a user account with sudo privileges and configured for passwordless sudo access.
- **Debian 12 UTM Gallery Image Users**: If you are using the Debian 12 gallery image from UTM, no initial setup for passwordless sudo is required. The script will automatically configure the necessary sudoers file. Simply ensure that your VM has an active internet connection, and you can run the script immediately after a fresh installation.
- While it's not mandatory to install additional dependencies, it is highly recommended to use `tmux` or `screen`, especially when running the script over SSH. These tools help maintain your session and build progress in case of network disruptions.

### Setup

The script can be integrated into your system in several ways:
- Execute it directly whenever needed.
- Add the script to your `.bashrc` file for automatic initialization. You can do this by adding a alias to your bashrc like this:
```
alias whonix="/bin/bash $HOME/.config/whonix-script/whonix"
```
- Place the script in `/usr/bin` for system-wide accessibility.
```
$ sudo cp whonix /usr/bin/
```

Please ensure you read and understand the script before running it to familiarize yourself with its functions and operations.

### Running the Script

To build Whonix, invoke the script with the version tag of Whonix you wish to build as the argument. For example:

```
$ whonix 17.1.1.8-developers-only
```

Upon successful completion of the script, the resulting `.tar.gz` archives for both the Whonix Workstation and Gateway will be located within a directory named `whonix-binary` in your home directory. This directory will also contain the build log for your reference.

To transfer the `whonix-binary` folder to your Mac, the `scp` command can be utilized. Once moved, you can extract the contents of both the Workstation and Gateway `.tar.gz` files using the command `tar -xvf` to obtain the UTM-compatible files. Following extraction, these files can be run in UTM to initiate your Whonix instances.

### Optional: Verifying the Signing Key

After running the script, it is a good security practice to verify the signing key of the downloaded Whonix files. Verifying the digital signature ensures that the files have not been tampered with and are indeed from a trusted source. For detailed instructions on how to perform this verification, please refer to [Whonix's Official Signing Key Verification Guide](https://www.whonix.org/wiki/Signing_Key).

### Questions and Issues

If you have any questions or encounter any issues, please feel free to contact me directly or open an issue on this repository. Your feedback and contributions are welcome, whether they are bug reports or feature requests.

Thank you for using this script to build Whonix on your Apple Silicon Mac.
