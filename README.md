# ShellTips
Tools &amp; code snippets

Print a text file or a config file without comments:

```
cat /etc/squid/squid.conf | egrep -v "^\s*(#|$)"
```
