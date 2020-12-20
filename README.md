## SELinux, Seecurity Enhance Linux —

Security-Enhanced Linux is a Linux kernel security module that provides a mechanism for supporting access control security policies, including mandatory access controls. SELinux is a set of kernel modifications and user-space tools that have been added to various Linux distributions. 

### Mode of SELinux —

1. Enforcing
2. Permissive
3. Disabled


### Status show details —

[root@192 ~]# sestatus

```
SELinux status:                 enabled
SELinuxfs mount:                /sys/fs/selinux
SELinux root directory:         /etc/selinux
Loaded policy name:             targeted
Current mode:                   permissive
Mode from config file:          enforcing
Policy MLS status:              enabled
Policy deny_unknown status:     allowed
Memory protection checking:     actual (secure)
Max kernel policy version:      32
```


### Policy consists of User, Role and Domains — 

[root@192 ~]# semodule -l | less

[root@192 ~]# semanage boolean -l | less

[root@192 ~]# getsebool cron_system_cronjob_use_shares

```cron_system_cronjob_use_shares --> off```

[root@192 ~]# setsebool cron_system_cronjob_use_shares on

[root@192 ~]# getsebool cron_system_cronjob_use_shares

```cron_system_cronjob_use_shares --> on```
