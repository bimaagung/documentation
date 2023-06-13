Buatkan dokumen secara rapi install solaar

To resolve this issue, you can try reinstalling Solaaar using pip. Here are the steps you can follow:

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
   sudo solaar <command> (show ,pair, unpair)
   ```
7. Pastikan bluetooth menyala dan mode pair
8. Hubungkan usb Mouse M720
9. Pastikan moouse logitech M720 dalam mode pair

10. Connectkan ke 
   ```
   sudo solaar pair
   ```
11. Apabila masih tidak menyala , silahkan off kan dulu mousenya dan on kan kembali

