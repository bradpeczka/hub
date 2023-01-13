# Description

A parser for the Proxmox Mail Gateway (PMG) web admin interface.
pmgdaemon listens on port 8006/tcp and writes authentication fails into syslog 

# Logs

  - Error

```
Jan 13 11:32:07 pmgdev pmgdaemon[1183]: authentication failure; rhost=::ffff:ffff:192.0.2.1 user=toor@pam msg=no such user ('toor@pam')
Jan 13 11:32:26 pmgdev pmgdaemon[1183]: authentication failure; rhost=::ffff:192.0.2.1 user=root@pam msg=auth failed: Authentication failure
```

> In the first string, the user does not exist.
> In the second string, the user exists but authentication fails.

  - Success

```
Jan 13 11:31:36 pmgdev pmgdaemon[1183]: successful auth for user 'root@pam'
```

# To be done

  - ?

# Explain output

  - proxmox-pmg-logs parser is used only for authentication failures.

```
<samples>
```