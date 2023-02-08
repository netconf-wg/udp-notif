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
$ pyang ietf-udp-notif-transport.yang -p draft-yangs -f tree --tree-line-length=70 --tree-depth=6
```

To generate draft .txt
```shell
$ xml2rfc <draft>.xml
```

UDP-notif
---------
[x] IANA on the version number of to allow the reference of the legacy draft
[x] presence yang container instead of the flag + dtls params
[x] Controlled environments definition on the draft, to help understand the dtls layer (feedback Benoit)
[x] Security considerations at the end of the draft
[x] revise BSD license
[x] Add subsection to IANA
[x] TLS as normative ref
[ ] Confirm to Mahesh when to send it to sec WG to confirm the dtls layer is ok
[ ] Operational consideration Section when DTLS is used with UDP-notif
[ ] prefix un to sn -> Ask why https no?
[ ] why ip address with a zone 
[x] add rfc8040 tree diagrams -> Ask Tom --> add reference !
[/] Add phrase for one message id sequence for a observation domain id --> ask to the ML
[x] when options are not in order -> MAY be dropped
[ ] Use HTTPS-notif YANG module for consistency
