Amazon Linux AMI Base
=====================

This role intends to provide some enhancements to Amazon Linux AMI base environment.

Requirements
------------

Boto Python module required

    $ sudo pip install boto

Role Variables
--------------

Change variables under `defaults/main.yml`. All variables used in this role are mentioned here.

Example Playbook
----------------

    - hosts: your_amazon_servers
      roles:
        - { role: include.amzn-base }

Applying the playbook
---------------------

If using a local inventory:

    export ANSIBLE_HOSTS=ansible_hosts

    $ ansible-playbook \
        -e aws_access_key=${AWS_ACCESS_KEY_ID} \
        -e aws_secret_key=${AWS_SECRET_ACCESS_KEY} \
        -e aws_region=${AWS_REGION} \
        playbook.yml

or if you have AWS credentials defined in your environment:

    $ export AWS_ACCESS_KEY_ID=foo
    $ export AWS_SECRET_ACCESS_KEY=bar
    $ export AWS_REGION=baz

just run it like:

    $ ansible-playbook playbook.yml

License
-------

BSD

Author Information
------------------

Francisco Cabrita <francisco.cabrita@gmail.com>