## EX.NO : 03
## DATE : 7.9.2023
# <p align="center">Enumeration</p>

Explore Google hacking and enumeration
## AIM:
To use Google for gathering information and perform enumeration of targets

## STEPS:
### Step 1:
Install kali linux either in partition or virtual box or in live mode

### Step 2:
Investigate on the various Google hacking keywords and enumeration tools as follows:

### Step 3:
Open terminal and try execute some kali linux commands

### Pen Test Tools Categories:
Following Categories of pen test tools are identified: Information Gathering.

### Google Hacking:
Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

### site:
This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain. Following searches for all the sites that is in the domain youtube.com
![239508324-d0ee0a18-5466-4890-b856-6b6b5d4c90bb](https://github.com/durga46/Enumeration/assets/75235704/6cb4c1ea-06ce-45fc-8e23-60592f348ab5)



### filetype:
This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files. Following searches for pdf file in the domain youtube.com

![239508902-f1d252cf-b572-4806-9f38-8bc11c07e0f0](https://github.com/durga46/Enumeration/assets/75235704/41f3f1c3-9dc4-4367-afc6-30ce97fcca77)


### intext:
This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.
![239509731-ac90bd1e-0b2d-4fee-a6af-1d7a5829e103](https://github.com/durga46/Enumeration/assets/75235704/7d3e61a3-d77a-4f37-8eb1-a6b0dc4a7ab0)



### inurl:
This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![239510385-4a68f26c-41da-4e81-a3a7-9bc83c3344e8](https://github.com/durga46/Enumeration/assets/75235704/30926370-d25a-4e8e-a562-b6a5137a15b4)



### intitle:
This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
![239511674-b749a39a-ebae-4e03-9a75-43ba98beb18a](https://github.com/durga46/Enumeration/assets/75235704/b7639e34-ce34-4b61-8392-8b83407aa540)



### link:
This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

![239513103-e7524e6d-ccb0-4b3a-b8f6-250cd841747a](https://github.com/durga46/Enumeration/assets/75235704/b0a795a2-614a-4be4-9216-44613e30bf13)


### cache:
This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.

![239512809-1b274012-225e-4153-b4f6-ccc1fd307cde](https://github.com/durga46/Enumeration/assets/75235704/e59d671f-d48e-476b-a37d-e9eb839bca26)


# DNS Enumeration
## DNS Recon
provides the ability to perform: Check all NS records for zone transfers Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT) Perform common SRV Record Enumeration Top level domain expansion

## OUTPUT:

![241196881-e27b6257-4d38-4365-a04f-6bd71610632a](https://github.com/durga46/Enumeration/assets/75235704/e4b43bb5-77e5-4e7b-99fb-ad16aa5f6a02)

### dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record). Get the namservers (threaded). Get the MX record (threaded). Perform axfr queries on nameservers and get BIND versions(threaded). Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”). Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded). Calculate C class domain network ranges and perform whois queries on them (threaded). Perform reverse lookups on netranges (C class or/and whois netranges) (threaded). Write to domain_ips.txt file ip-blocks. This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
![241198023-795c489d-ba57-4e77-9791-49c71fc3f4d3](https://github.com/durga46/Enumeration/assets/75235704/0e4b62ab-63d3-4703-9cb9-d2b6ca2ef992)

### smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
![241410635-c41be6f0-d0d4-40eb-9074-136cabe5c74b](https://github.com/durga46/Enumeration/assets/75235704/191b4c82-acda-495b-9ad7-e4bda8bab48a)



In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
![241408341-ba786664-2105-44aa-ab07-465057083629](https://github.com/durga46/Enumeration/assets/75235704/ed1a12e8-5a1b-4d5f-8c98-44cc24c1a613)



select any username in the first column of the above file and check the same
![241408615-ad0d26fe-7a60-4604-be93-1bf950d88646](https://github.com/durga46/Enumeration/assets/75235704/6df102c3-4dfc-4bca-991a-79c14d9fde0f)



### Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25 telnet 25 to connect and issue appropriate commands

### Output:
![241409971-4fd9ca59-abdf-43bc-917c-71e2c7e4351d](https://github.com/durga46/Enumeration/assets/75235704/5b8467a6-7856-4a57-ab9d-e4a365e00e08)


### nmap –script smtp-enum-users.nse 
The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.
## Output:
![268923880-9bd4c245-dd84-4517-bf27-12a7cd3c070b](https://github.com/durga46/Enumeration/assets/75235704/b5f26048-51bb-4bd9-80aa-af1ae62a90e8)




RESULT:



The Google hacking keywords and enumeration tools were identified and executed successfully
The Google hacking keywords and enumeration tools were identified and executed successfully
