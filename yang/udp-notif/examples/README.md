
```shell
$ pyang -f sample-xml-skeleton -p dependencies --sample-xml-skeleton-doctype=config -V --sample-xml-skeleton-defaults dependencies/ietf-subscribed-notifications@2019-09-09.yang dependencies/ietf-yang-push@2019-05-21.yang dependencies/ietf-subscribed-notif-receivers@2022-11-03.yang ietf-udp-notif-transport@2025-04-27.yang -o examples/ietf-udp-notif-example-21.xml 
```

```shell
$ pyang -f tree -p draft-yangs -V /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-subscribed-notifications.yang /Users/ahuangfeng/.pyenv/versions/3.9.5/share/yang/modules/ietf/ietf-yang-push.yang draft-yangs/ietf-subscribed-notif-receivers.yang ietf-udp-notif-transport.yang
```

```shell
$ ./rfcfold.sh -s 1 -i ietf-udp-notif-example-21withoutDTLS.xml -o example_rfc8792.xml
```


Validating without DTLS
```bash
$ /home/vagrant/Unyte/libyang/build/yanglint -p ./dependencies dependencies/ietf-netconf@2011-06-01.yang dependencies/ietf-subscribed-notifications@2019-09-09.yang dependencies/ietf-yang-push@2019-05-21.yang dependencies/ietf-subscribed-notif-receivers@2022-11-03.yang ietf-udp-notif-transport@2025-04-27.yang dependencies/ietf-datastores@2018-02-14.yang examples/ietf-udp-notif-example-21withoutDTLS.xml
```

Validating with DTLS
```bash
$ /home/vagrant/Unyte/libyang/build/yanglint -p ./dependencies dependencies/ietf-truststore@2024-10-10.yang dependencies/ietf-crypto-types@2024-10-10.yang dependencies/ietf-tls-common@2024-10-10.yang dependencies/ietf-tls-client@2024-10-10.yang dependencies/ietf-datastores@2018-02-14.yang dependencies/ietf-subscribed-notifications@2019-09-09.yang dependencies/ietf-yang-push@2019-05-21.yang dependencies/ietf-subscribed-notif-receivers@2022-11-03.yang ietf-udp-notif-transport@2025-04-27.yang examples/ietf-udp-notif-example-21withDTLS.xml
```
