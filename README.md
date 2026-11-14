# NETWORKWALKsRaymart-B084-WK2-PM1 PM2-CYBERSECURITY-LAB-SETUP
Networkwalks Week 2 Project Module 1

Task 1 
$ whois networkwalks.com

<img width="1912" height="1075" alt="whois" src="https://github.com/user-attachments/assets/73b2fcf4-7837-412e-a1f2-d4e36e82390c" />

whois reveals the registrar, registration and expiry dates, and name servers. Here the name
servers point to HostGator, so an attacker instantly learns the hosting provider. Registration dates
and abuse contacts help with social engineering and planning.

Task 2
$ whatweb networkwalks.com

<img width="1917" height="1078" alt="Screenshot 2026-11-12 093917" src="https://github.com/user-attachments/assets/92016e90-268a-4e5f-adb3-f17d54ccbc10" />

whatweb exposes the exact software and versions (here Wordpress 7.1.4 and WP Download
Manager 3.3.76). An attacker looks these versions up in vulnerability databases to find known
exploits. It also leaks the server IP and an email address.

Task 3
$ nslookup networkwalks.com

<img width="1917" height="1078" alt="nslookup and woof" src="https://github.com/user-attachments/assets/898846d0-a561-4fd2-8ec8-0c94b5e348a8" />

nslookup turns a domain name into its real IP address (192.232.216.135). Knowing the IP lets an
attacker scan the server directly, look up other sites on the same IP, and map the target's
infrastructure.

Task 4
$ curl -I https://networkwalks.com

<img width="1917" height="1061" alt="curl" src="https://github.com/user-attachments/assets/0486ebd7-4831-4964-9d46-b5c714789395" />

HTTP headers leak the web server, caching stack and hidden endpoints (here the WordPress
REST API at /wp-json/). Attackers read headers to fingerprint the stack and find entry points
without even loading the full page.

Task 5
$ wafw00f networkwalks.com

<img width="1917" height="1078" alt="nslookup and woof" src="https://github.com/user-attachments/assets/49fe1d08-840d-4f52-a576-2b6f3ce54996" />

Task 6
$ dnsrecon -d networkwalks.com

<img width="1920" height="1080" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/6cc49079-76cd-493d-a782-deef2629cf25" />

dnsrecon maps the target's entire DNS footprint: mail servers, DNS software version (Bind
9.16.23), SPF policy and cPanel service records. Each record is a potential foothold and helps an
attacker understand the email and hosting setup.

WHY FOOTPRINTING MATTERS?

Reconnaissance is the first stage of every real attack. Before touching a target, an
attacker quietly builds a complete profile of it using only public information, exactly the
tools in this task. whois and DNS tools (nslookup, dnsrecon) reveal who owns the
domain, its real IP address, its hosting provider and its mail servers. whatweb and curl
fingerprint the exact software and versions running, which an attacker matches against
known vulnerabilities. wafw00f warns them whether a firewall is watching, so they know
how careful to be.
None of these tools attack the target. They only read what is already public, which is
exactly why footprinting is so powerful and so hard to detect. The more an organization
leaks, the easier every later stage of the attack becomes. This is also why defenders
run the same tools on themselves: to see what an attacker would see, and to reduce it.

WEEK 2 PM5

Zenmap Network Scanning (Practice Lab)

<img width="1647" height="878" alt="Screenshot 2026-11-14 011944" src="https://github.com/user-attachments/assets/a58e8b29-99ea-4b10-a845-f94ffe197f05" />

<img width="1647" height="876" alt="Screenshot 2026-11-14 012105" src="https://github.com/user-attachments/assets/87b3ab6d-68b9-48c4-9f25-063c0a4a9063" />



