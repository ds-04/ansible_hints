# ansible_hints
ansible_hints


<h1>Ad hoc commands</h1>

Ad hoc commands default to command module. Or you can provide -m to use a moudle, e.g. ping.

Check the log size of some log

``ansible all -a "sudo du -hs /var/log/some_log``



<h1>Dictionaries and loops</h1>

