Reboot your Kali Linux system into the GRUB boot menu. Highlight the default boot menu you are usually booting from and press the `e` key in order to edit this boot menu entry.

2.  Edit GRUB menu

[![Enter GRUB edit mode](https://linuxconfig.org/images/02-how-to-reset-root-password-kali-linux.png)](https://linuxconfig.org/images/02-how-to-reset-root-password-kali-linux.png "Enter GRUB edit mode")

Once you entered the GRUB menu edit mode you will be presented with the following window. Scroll down until you hit the line starting with keyword `linux`.

[![Edit GRUB menu entry](https://linuxconfig.org/images/03-how-to-reset-root-password-kali-linux.png)](https://linuxconfig.org/images/03-how-to-reset-root-password-kali-linux.png "Edit GRUB menu entry")

After you have located the appropriate boot entry as specified by the previous step, use navigational arrows to look for keyword `ro` and replace it with keyword `rw`. Next, on the same boot entry find keyword `quiet` and replace it with `init=/bin/bash`.

---

---

5.  Check RW permissions on root partition

[![Confirm root partition permissions](https://linuxconfig.org/images/04-how-to-reset-root-password-kali-linux.png)](https://linuxconfig.org/images/04-how-to-reset-root-password-kali-linux.png "Confirm root partition permissions")

Type `mount` command and look for `/` root mount partition. Confirm that this partition is mounted with `rw` permissions.

7.  Reset Kali root password

[![Reset root password - kali linux](https://linuxconfig.org/images/05-how-to-reset-root-password-kali-linux.png)](https://linuxconfig.org/images/05-how-to-reset-root-password-kali-linux.png "Reset root password - kali linux")

At this point we are ready to reset the root user password. Type `passwd` command and enter your new password. Enter the root password again to verify. Press `ENTER` and confirm that the password reset was successful.

9.  Reboot Kali