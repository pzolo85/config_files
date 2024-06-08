# Initial setup 
- List of tasks that I like to run once when setting up a new system. 

## Set vim as default editor
- `sudo update-alternatives --config editor` 

## Run sudo without password 
- Edit sudoers file with `sudo visudo` 
- Allow users in the `sudo` group to run all commands without asking for password: `%sudo   ALL=(ALL:ALL) NOPASSWD:ALL`

## Remap Caps Lock to escape
- Find out the keymap of each key with `xdev` (capslock should be 66, esc 9)
- List all the mappings with `xmodmap -pk`
- Remap wiht: `xmodmap -e 'keycode 66 = Escape'` 

## Remap Caps Lock to escape (updated)
- Revert the changes in xmodmap 
- Edit the `/etc/default/keyboard` file and include: `XKBOPTIONS="caps:escape"`
- reboot 
