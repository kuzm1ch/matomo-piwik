Matomo (piwik)
=========

Matomo, formerly Piwik, is a free and open source web analytics application developed by a team of international developers, that runs on a PHP/MySQL webserver.

Requirements
------------

Python 2 is required on target instance because mysql-python module is not working properly with python3(related to base image Ubuntu 16.04 from AWS).  
Also you can find [molecule](https://molecule.readthedocs.io/en/latest/) directory, it is tool for testing purpose.

```
sudo apt install python3.6-dev
virtualenv --python=/usr/bin/python3.6 python3.6
source python3.6/bin/activate
pip install docker-py
pip install ansible molecule
cd role/matomo-piwik & molecule test
```

Example Playbook
----------------
`ansiple-playbook -i inventory matomo.yml`
