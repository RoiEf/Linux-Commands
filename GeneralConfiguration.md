# General configuration options

### Enable Numlock on login
The default configuration file for SDDM can be found at /usr/lib/sddm/sddm.conf.d/default.conf.
```
[General]
# Initial NumLock state. Can be on, off or none.
# If property is set to none, numlock won't be changed
# NOTE: Currently ignored if autologin is enabled.
Numlock=on
```