Using only sync waves is a good way to change the resource ordering but they still suffer from some limitations

Sync wave numbers are "global" for the whole application
There are some known limitations with jobs and sync waves that might affect you
You can combine sync waves and phases in a single application. If you do that then sync wave numbers are "scoped" to their respective sync phase making their management a bit easier.


cleanup.yml -> PostSync, wave 20
db-upgrade.yml -> PreSync, wave 10
disable-alerts.yml -> PreSync, wave 20
enable-alerts.yml -> PostSync, wave 30
grafana-notify.yml -> Sync, wave -10
slack-notify.yml -> PostSync, wave 30
smoke-test.yml -> PostSync, wave 10
