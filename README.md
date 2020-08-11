# Nagios check_Memory Service For the Linux systems.

how to automate the check_memory service in Nagios.

The Nagios Plugins for Linux are intended to be run by NRPE, the Nagios Remote Plugin Executor, that "allows you to remotely execute Nagios plugins on other Linux/Unix machines. This allows you to monitor remote machine metrics (disk usage, CPU load, etc.)."

Plugin name : check_memory which will checks the memory usage in a linux machine. 

You can create your own plugin or you can download from Nagios: https://exchange.nagios.org/components/com_mtree/attachment.php?link_id=3407&cf_id=24

Once download keep the script in the tmp directory and then run the ansible playbook: ansible-playbook -i hosts check_mem.yml and you can configure the memory service in Nagios

Example:
./check_memory.sh -u -w 80 -c 95
w: warning
c : critical
u : used
