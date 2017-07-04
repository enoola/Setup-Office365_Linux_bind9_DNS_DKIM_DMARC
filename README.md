# Setup Office365 and Linux to have mail trusted from your own domain

Configure Linux bind9 DNS with Office365 (DKIM and DMARC also)

Why this documentation ? :
  It's more a note than anything, since I couldn't find any clear documentation on the matter, knowing that I will need to redo it at some points, notes are of importance, moreover if it can help others...

### Pre-requisite :  
 * a Microsoft Office 365 Business Premium or Business Essentials account (Trial or Pro) with full admin rights 
 * a Linux server with root rights    
 * a domain name that you own

### Let's start :  
 * Few infos and Screenshots of What you should have access to 
	[Verify you have what it takes](docs/startoverview.md)

### Configuration :  
 * Setup office 365 with a personnal owned domain name
 * Setup DKIM (Domain Key Identified Mail) for Office 365
 * Setup DMARC (Domain-based Message Authentication, Reporting and Conformance (DMARC) for Office 365


### Useful documentations to achieve this :    
 * Setup DKIM for office 0365 : <https://technet.microsoft.com/en-gb/library/mt695945(v=exchg.150).aspx>  
 * tuto to setup O365 : <https://blog.kaniski.eu/2014/07/office-365-and-bind/>  
 * DKIM Validator : <http://dkimvalidator.com/results>  
 * Setup SPF to prevent spoofing : <https://technet.microsoft.com/en-us/library/dn789058(v=exchg.150).aspx>  

# Verify you are not consider as a :  
 * scatter : http://www.backscatterer.org/index.php 
 * spammer : http://www.uceprotect.net/en/rblcheck.php


 



