# Overview

This is a basic rundown of ansible commands

- - - -
# Commands

Install ansible and a yaml linter

    pip install ansible --user

    pip install yamllint --user

    alias yams='find . -type f -name "*.yml*" | sed "s|\./||g" | egrep -v "(\[warning\])" | xargs yamllint -f parsable'

    yams

Adhoc commands


Targetting a group

    ansible -i inventory fleet -m ping

    ansible -i inventory fleet -m shell -a "uptime"

    ansible -i inventory fleet -m shell -a "free -mt"

Running your first playbook

    ansible-playbook -i inventory playbook.yml

