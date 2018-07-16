# dvorak-de
In this package you will find a german dvorak keymap for kbd.
Follow these instructions to enable it at boot:

### Prepare the file
Download the file and name it "dvorak-de.map"      
In console navigate to the folder where you stored it.       
Then run:
```
gzip dvorak-de.map
```
The result is "dvorak-de.map.gz".
Run
```
cp dvorak-de.map.gz /usr/share/kbd/keymaps/i386/dvorak/
```
Then you should run 
```
chown root:root /usr/share/kbd/keymaps/i386/dvorak/dvorak-de.map.gz
```

After adding `KEYMAP=dvorak-de`  to your `/etc/vconsole.conf`
run `mkinitcpio -p linux`. 

After reboot dvorak will be the keyboard layout, for console.

<aside class="notice">
Careful: This will also change the keyboard-layout for the encryption password.
Make sure, you will be able to enter it in dvorak. Otherwise you will lock yourself out of your machine.
  </aside>
