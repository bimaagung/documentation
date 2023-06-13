Here is the properly formatted document for installing Solaaar:

To resolve this issue, you can try reinstalling Solaaar using pip. Follow the steps below:

1. Open a terminal.

2. Activate the root user by running the command:
   ```
   sudo -i
   ```

   Enter your password when prompted.

3. Once you are in the root user environment, reinstall Solaaar using pip:
   ```
   pip install --force-reinstall solaar
   ```

   The `--force-reinstall` flag ensures that the package is reinstalled even if it's already installed.

4. After the installation is complete, exit the root user environment by running the command:
   ```
   exit
   ```

5. Verify if Solaaar is working correctly by running the command:
   ```
   solaar --version
   ```

6. Run the `solaar` command with root privileges using `sudo`:
   ```
   sudo solaar <command> (show, pair, unpair)
   ```

7. Ensure that Bluetooth is turned on and in pairing mode.

8. Connect the Logitech M720 mouse via USB.

9. Make sure the Logitech M720 mouse is in pairing mode.

10. Connect the device using the command:
    ```
    sudo solaar pair
    ```

11. If the issue persists, try turning off the mouse and turning it back on again.

These are the steps you can follow to install Solaaar and connect the Logitech M720 device. If you have any further questions or need additional assistance, feel free to ask. I'm here to help!
