HOWTO
=====

    ansible-playbook site.yml

Add `-u <user>` to login with a name different than your local login-name (defaults in ansible.cfg).
Add `-l <host or group>` to limit the playbook to just that/those host(s).
Use `-e ansible_ssh_port` to change the ssh port used (defaults in ansible.cfg).

AWS
===

You'll need boto (python-boto on Debian, python2-boto on Arch) and access key id and secret and region from AWS exported:

    export AWS_ACCESS_KEY_ID=...
    export AWS_SECRET_ACCESS_KEY=...
    export region=..
