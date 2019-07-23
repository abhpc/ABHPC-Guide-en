# Administrator and User Guide for ABHPC

### 1. Introduction

ABHPC is a diskless based linux cluster system, which is focusing on the high performance computing. Compared with the common diskless clusters, ABHPC can be built completely based on a single Infiniband network (of course, it can also be built based on 1 Gigabit or 10 Gigabit Ethernet). All software used by ABHPC is open source and free. However, building such a system takes a lot of time and effort and requires a fairly high level of professionalism. It is unrealistic to understand the construction of the entire ABHPC system through a single project. Actually, the capability of the ABHPC system is exactly identical with the current mainstream super-computing centers all over the world, and its professional standards are no less than those of the super-computing centers.

This project is mainly provided to administrators and users of the ABHPC system. The author can provide paid services to those who want to build an ABHPC system. The price starts at least $2,000 depending on the scale of the system, which is calculated by at an hourly pay of $50. Again, the author provides services but NOT software. Any commercial software needs to be certified by the users. If you are interested in ABHPC system, you can contact me by sending an email (xyliucd#AT#foxmail.com).

The basic Linux system for ABHPC is CentOS 7 or Ubuntu 16.04 LTS. The job scheduling system used in ABHPC is slurm.

### 2. Instruction

According to the rules in Linux, **the sign "#" at the head of a command means a root's privilege, and sign "$" means common user's.** Fresh users should read [Common commands in Linux](User/Linux_commands.md) first.

Some commands in ABHPC are developed by the author, which will not be elaborated in this project.

### 3. Structure of This Project

#### For Common Users

[Connect to the master node by ssh client.](User/ssh_client.md)

[Remote graphical desktop (MATE desktop) by x2go.](User/x2go.md)

[How to use slurm to run jobs.](User/slurm_user.md)

[Common sbatch scripts.](User/slurm_script)

[Common errors.](User/errors.md)

[Useful knowledge for high performance computing.](User/knowledge.md)

#### For Administrators

[Add a user in ABHPC system.](Admin/add_user.md)

[How to manage the slurm system.](Admin/manage_slurm.md)

[Set up a MATE desktop for x2go users.](Admin/x2go_server.md)

[Install common software.](Install_software)
