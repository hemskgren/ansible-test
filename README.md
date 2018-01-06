# ansible-test
Ansible playbooks for test and verification of rundeck and semaphore.

run by:
ansible-playbook inventory.yml  --extra-vars="hosts_vars=lan-dev username=userid password=mypwd"


###
ansible-playbook --list-tasks lan_verify.yml -e "hosts_vars=none"

playbook: ios_verify.yml

  play #1 (Switch): Switch	TAGS: []
    tasks:
      verify arp and interface on devices	TAGS: []
      switch fail	TAGS: []
      Send notification message via Slack all options	TAGS: []

  play #2 (AP): AP	TAGS: []
    tasks:
      verify wifi, ntp and interface on devices	TAGS: []
      AP fail	TAGS: []
      Send notification message via Slack	TAGS: []

  play #3 (ASA): ASA	TAGS: []
    tasks:
      verify inv, route, arp and ntp	TAGS: []
      asa fail	TAGS: []
      Send notification message via Slack all options	TAGS: []
