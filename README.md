# yubikey under linux #

# Roles #

## pam-u2f ##

Tested with:
* fedora 30

### Requiaments ##

*  yubikey with u2f support

### Install tools and config for gdm pam and sudo ###

Enter:
```bash
sudo ansible-playbook ./setup_pam.yml
```

### Add your u2f key ###

With the command 'pamu2fcfg' can you get your pubic u2f key. Put your hardware key in and Enter:
```bash
mkdir -p ~/.config/Yubico && pamu2fcfg >> ~/.config/Yubico/u2f_keys
```
Push the button on your key when the light gon on (do you have only 15 secons time for this).

### External docu ###

* https://developers.yubico.com/pam-u2f/
* https://wiki.gentoo.org/wiki/Pam_u2f
* https://infosec-handbook.eu/blog/yubikey-2fa-pam/
