
```shell
$ pyang -f sample-xml-skeleton -p draft-yangs --sample-xml-skeleton-doctype=config -V --sample-xml-skeleton-defaults /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-subscribed-notifications.yang /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-yang-push.yang draft-yangs/ietf-subscribed-notif-receivers.yang ietf-udp-notif-transport.yang -o examples/ietf-udp-notif-example-09.xml 
```

```shell
$ pyang -f tree -p draft-yangs -V /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-subscribed-notifications.yang /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-yang-push.yang draft-yangs/ietf-subscribed-notif-receivers.yang ietf-udp-notif-transport.yang
```

```shell
$ ./rfcfold.sh -s 1 -i ietf-udp-notif-example-09withoutDTLS.xml -o example_rfc8792.xml
```
