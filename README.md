# ralph-scan


```
$ ralph-scan -h

Usage: ralph-scan [IP... [--components] [--plugins] [--dry-run]] COMMAND [arg...]

Easy way to scan your devices

Arguments:
  IP=[]        IP or HOSTNAME device to scan

Options:
  --components=[]   List components to scan. Available components:
                    CPU, RAM, DISK, ETHERNETS, DISK-SHARES ($RALPH_SCAN_COMPONENTS)
  --plugins=[]           Ralph scan plugins to run. Available plugins: PLUGIN1, PLUGIN2 ($RALPH_SCAN_PLUGINS)
  --dry-run=false        Only show scan results, not send to Ralph ($RALPH_SCAN_DRY_RUN)
  --device-template=""   Ready to use plugin and components pack to scan typical
                         devices. Available templates: IDRAC, ILO, XEN  ($RALPH_SCAN_DEVICE_TEMPLATE)
  -v, --version    Show the version and exit

Commands:
  generate-config   Generate Ralph-Scan config in ~/.ralph-scan/config.yml

Run 'ralph-scan COMMAND --help' for more information on a command.
```

## create config file
```
./ralph-scan generate-config -h

Usage: ralph-scan generate-config

Generate Ralph-Scan config in ~/.ralph-scan/config.yml
```

## example config file

```
global:
  auth:
    username: ralph
    password: ralph
plugins:
  - ILO
  - IDRAC
  - IPMI
```
