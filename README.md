# IETF Drafts

## Requirements
- pyang (tested in pyang==2.5.3)
- xml2rfc

## UDP-notif

To generate YANG tree
- Check if client-server drafts are updated first.

```shell
$ cd yang/udp-notif
$ ln -s ietf-notif-06.yang ietf-notif.yang
$ pyang ietf-udp-notif.yang
$ pyang -f tree ietf-udp-notif.yang -p draft-yangs
$ pyang ietf-udp-notif-transport.yang -p draft-yangs
$ pyang ietf-udp-notif-transport.yang -p draft-yangs -f tree --tree-line-length=69 --tree-depth=6
```

To generate draft .txt
```shell
$ xml2rfc <draft>.xml
```
