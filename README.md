# Bash SNIPPETS

Tools &amp; code snippets

Print a text file or a config file without comments:

```SH
cat /etc/squid/squid.conf | egrep -v "^\s*(#|$)"
```

Toggle ON/OFF "Scroll Lock", useful with cheap backlit keyboards

```SH
#!/bin/bash
kbled=$(xset -q | grep 'Scroll Lock:' | cut -d ":" -f 7)
if [ $kbled == "off" ]; then
   xset led named "Scroll Lock"
else
   xset -led named "Scroll Lock"
fi
```
