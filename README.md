# ansible_hints
ansible_hints


<h1>Ad hoc commands</h1>

Ad hoc commands default to command module. Or you can provide -m to use a moudle, e.g. ping.

Check the log size of some log (you may need sudo for this example, before the du)

``ansible all -a "du -hs /var/log/some_log"``



<h1>Dictionaries and loops</h1>



<h1>Limit to host range using seq</h1>

``ansible-playbook playbook.yml -l $(seq -s, -f 'hostname1%03g' 01 26)``
