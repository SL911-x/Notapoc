<h1 align="center">
  <br>
  <a href=""><img src="/img/logo.png" alt="" width="300px;"></a>
  <br>
  <img src="https://img.shields.io/badge/PRs-welcome-blue">
  <img src="https://img.shields.io/github/last-commit/kh4sh3i/CVE-2023-22515">
  <img src="https://img.shields.io/github/commit-activity/m/kh4sh3i/CVE-2023-22515">
  <a href="https://twitter.com/intent/follow?screen_name=kh4sh3i_"><img src="https://img.shields.io/twitter/follow/kh4sh3i_?style=flat&logo=twitter"></a>
  <a href="https://github.com/kh4sh3i"><img src="https://img.shields.io/github/stars/kh4sh3i?style=flat&logo=github"></a>
</h1>


# CVE-2023-22515
CVE-2023-22515, a critical vulnerability affecting on-premises instances of Confluence Server and Confluence Data Center, a Broken Access Control vulnerability. Attlassian has provided a CVSS base score of 10.0



## One line poc
```
cat file.txt| while read host do;do curl -skL "http://$host/setup/setupadministrator.action" | grep -i "<title>Setup System Administrator" && echo $host "is VULN";done
```




## Nuclei
```
nuclei -u target -t CVE-2023-22515.yaml
```

## Prerequisites
```
sudo pip install -r requirements.txt
```


## Usage
```
sudo python3 exploit.py --url [target]
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


## refrences
* [atlassian](https://confluence.atlassian.com/security/cve-2023-22515-privilege-escalation-vulnerability-in-confluence-data-center-and-server-1295682276.html)
* [nist](https://nvd.nist.gov/vuln/detail/CVE-2023-22515)