# Setup Linux bind record DMARC ( Domain-based Message Authentication, Reporting and Conformance ) for Office 365

Prior to this you should have created a user account associated with your own domain.  
 * [Setup office 365 with a personnal owned domain name](docs/O365_AddDomainFirstSteps.md)
 * [Setup Mail Account with our new binded domain](docs/O365_AddUserOnNewDomain.md)


1. Login to your linux server and add the 'selectors' :   

 ```bash
$ssh sd-53250.dedibox.fr
```  

2. Edit `/etc/bind/db.enrollme.eu`, add the below at the end of the file :  
Bare in mind DMARC is a text record in your DNS record.   
Make the change to reflect your domain...  

 ```bash
;MICROSOFT DMARC
;;fo : 1 -> report if any mechanism fails (fsp, dkim)
;;rua : sends aggregate XML reports to ....
;;ruf : send forensic reports to ...
_dmarc	   3600	IN	TXT	"v=DMARC1; pct=100; p=quarantine; fo=1; rua=mailto:enrollme.eu-verification@enrollme.eu;ruf=mailto:enrollme.eu-verification@enrollme.eu;"  
```

3. Once done you can simply verify your DMARC is well setup.
 <https://otalliance.org/resources/spf-dmarc-tools-record-validator>

* [Go back to the main page](../README.md)  
