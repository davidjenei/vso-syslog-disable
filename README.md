```
gcc -fPIC -shared -ldl -o noop-syslog.so noop-syslog.c
systemctl --user edit vso
```

```
[Service]
  Environment=LD_PRELOAD=/path-to-my-lib/noop-syslog.so
```
