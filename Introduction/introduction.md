# 1. What is Configuration management?
Configuration management typically mean writing some kind of state description for our servers, then using a tool to enforce that the servers are in that state: right
packages are installed, configuration files have the expected values and expected permissions, the right services are running, and so on.

# 2. What is Ansible?
Ansible refers to both the software and the company that runs the open source project. Michael DeHaan is the creator of Ansible the Software, and the former CTO of Ansible the company. In October 2015, Red Hat bought Ansible.

# 3. Advantages of Ansible
- Simple
- Agentless (No daemons)
- Powerful
- Secure
- Idempotency
- Push-based

# 4. Ansible Terminologies
- **Host** - Remote servers to configure.
- **Playbook** - A playbook describes which hosts to configure, and an ordered list of tasks to perform on those hosts.
- **Inventory** - The collection of hosts that Ansible knows about is called inventory.

# 5. How Ansible works?
1. Ansible will make SSH connection in parallel to hosts,
2. Generate a python script for first task,
3. Copy the script to hosts,
4. Execute the scripts on hosts,
5. Wait for the script to complete execution on all hosts,
6. Then move to next task in the list and go through these same four steps.
7. Important points
   - Ansible run each task in parallel across all hosts.
   - Ansible wait until all hosts have completed a task before moving to the next task.
   - Ansible runs the tasks in the order that you specify them.
