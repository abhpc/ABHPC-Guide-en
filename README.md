# Administrator and User Guide for ABHPC

### 1. Introduction

ABHPC is a diskless based linux cluster system, which is focusing on the high performance computing. Compared with the common diskless clusters, ABHPC can be built completely based on a single Infiniband network (Of course, it can also be built based on 1 Gigabit or 10 Gigabit ethernet). All software used by ABHPC is open source and free. However, building such a system takes a lot of time and effort and requires a fairly high level of professionalism. It is unrealistic to understand the construction of the entire ABHPC system through a single project. Actually, the capability of the ABHPC system is exactly identical with the current mainstream super-computing centers all over the world, and its professional standards are no less than those of the super-computing centers.

This project is mainly provided to administrators and users of the ABHPC system. The author can provide paid services to those who want to build an ABHPC system. The price starts at least $2,000 depending on the size of the system, which is calculated by at an hourly rate of $50. Again, the author provides services but NOT software. Any commercial software needs to be certified by the users. If you are interested in ABHPC system, you can contact me by sending an email (xyliucd#AT#foxmail.com).

遵循一般Linux系统的规则，**凡命令行开头为"#"的，表明此时正在使用root账户，而命令行开头为"$"的，则表明此时在使用普通用户**。建议没有Linux系统使用经验的用户，首先阅读[Linux常用命令](User/Linux常用命令.md)。

本教程中，部分命令是ABHPC特有的脚本命令，在此不再详细说明。

本项目针对普通用户和管理员提供以下教程：

### 1.普通用户

[ssh远程连接集群](User/ssh远程连接集群.md)

[远程桌面连接集群](User/使用x2go连接Ubuntu远程桌面.md)

[Slurm用户教程](User/Slurm用户教程.md)

[常见错误](User/常见错误.md)

[并行计算常用知识](并行计算常用知识)

### 2.集群管理员

新建集群用户: [CentOS 7](Admin/CentOS_7/新建集群用户.md)     [Ubuntu 16.04LTS](Admin/Ubuntu_16.04/新建集群用户.md)

[Slurm管理教程](Admin/Slurm管理教程.md)

[配置服务器的远程MATE桌面](Admin/配置服务器的远程MATE桌面.md)

[常用软件的安装](常用软件的安装)
