# PHP Reverse Shell

This repository contains a PHP script for implementing a reverse shell connection. Please note that reverse shells have legitimate use cases in various contexts, such as system administration and security testing. However, they can also be used maliciously. Therefore, use this script responsibly and only on systems you have permission to access.

## Disclaimer

The use of this script is subject to certain legal and ethical considerations. It is essential to understand and comply with the following terms:

- This tool may be used for legal purposes only.
- Users take full responsibility for any actions performed using this tool.
- The author accepts no liability for any damage caused by this tool.

If you do not agree with these terms, do not use this tool.

## Purpose

This PHP reverse shell script creates an outbound TCP connection to a specified IP address and port. Once connected, the recipient (the target server) will execute the provided shell command as the user running the web server (typically Apache). The script is designed for educational and testing purposes.

## Usage

To use this script, follow these steps:

1. **Edit the Script:** Open the script in a text editor and configure the following variables according to your needs:

   - `$ip`: Set the IP address of the listening server where the reverse shell will connect.
   - `$port`: Specify the port number on which the reverse shell will connect.
   - `$shell`: Define the shell command to execute on the target system. The default is `/bin/sh -i`.

2. **Upload the Script:** Upload the script to the target system where you want to establish a reverse shell connection. You can place it on a web server that runs PHP.

3. **Start a Listener:** On your listening server, set up a listener to accept the reverse shell connection. You can use tools like `netcat` or other reverse shell listeners.

4. **Execute the Script:** Access the script via a web browser or a similar method. The script will initiate the reverse shell connection to your listening server.

5. **Interact with the Shell:** Once the reverse shell is established, you can interact with the remote system as if you were using a terminal.

## Security Considerations

- **Legal and Ethical Use:** Ensure that you have proper authorization to use this script on a system. Unauthorized use may have legal consequences.

- **Secure Communication:** The communication between the script and the listening server is not encrypted. If used on a public network, consider using encryption or VPN to secure the connection.

- **Limited Error Handling:** The script has limited error handling and may terminate abruptly if any issues occur. Use with caution.

- **Cleanup:** After use, ensure that the reverse shell script is removed from the target system.

---

**Note:** This script is provided for educational purposes and as a reference. Always use it in accordance with applicable laws and permissions. Unauthorized and malicious use is strongly discouraged.
