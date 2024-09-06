# ansible_hints
ansible_hints


<h1>Ad hoc commands</h1>

Ad hoc commands default to command module. Or you can provide -m to use a moudle, e.g. ping.

Check the log size of some log (you may need sudo for this example, before the du)

``ansible all -a "du -hs /var/log/some_log"``



<h1>Dictionaries and loops</h1>



<h1>Limit to host range using seq</h1>

``ansible-playbook playbook.yml -l $(seq -s, -f 'hostname1%03g' 01 26)``

alternatively pregenerate colon seperated listing for ``-l``

`` echo node{0001..0010}|sed 's/ /:/g'``

<h1>Limit host range</h1>

Use -l

To exclude a host(s) though, use '!hostname1:!hostname2'

``ansible-playbook playbook.yml -l '!hostname'``


<h1>Paramiko issue</h1>

*Use at own risk*

Python got updated in the OS, but no pip or paramiko

```python -m ensurepip --upgrade```

To ensure the installed version of pip is at least as recent as the one available in ensurepip, pass the --upgrade option

Example python 3.12:

```
python3.12 -m ensurepip --upgrade
pip3.12 install paramiko
```





