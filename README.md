# ansible_image_build

Experiments in mounting a .raw image and using a chroot and Ansible to modify it.

`qemu-image convert` could be used to produce the raw from a qcow.

Currently it just installs `perl` which was not installed in the host.

Note the input image file is modified in-place.

Note this has to be run as root for the chroot connection to work, so:

    sudo su
    . venv/bin/activate
    ansible-playbook -v build.yml
