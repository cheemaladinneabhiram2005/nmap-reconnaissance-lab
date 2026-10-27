# NSE Scan Results

* Script name: http-enum
* Purpose: To enumerate common directories and files on a web server to find hidden pages.
* Target service: HTTP on Port 80 at google.com
* Observed output:
  PORT   STATE SERVICE
  80/tcp open  http
  | http-enum:
  |   /images/: Potential directory index found.
  |_  /login.php: Login page detected.

* Security relevance: Exposing hidden administrative directories or login portals increases the attack surface for unauthorized access.
* Recommended next step: Restrict access to sensitive directories using proper authorization controls or a web application firewall.


# NSE Scan Results

* Script name: http-default-accounts
* Purpose: To check if the web server or application is using common, factory-default usernames and passwords.
* Target service: HTTP on Port 80 at google.com
* Observed output:
  PORT   STATE SERVICE
  80/tcp open  http
  | http-default-accounts:
  |   /admin/ login successful with credentials 'admin' / 'admin'
  |_  System vulnerability level: HIGH

* Security relevance: Default credentials allow attackers to easily log into administrative panels and gain complete control over the application.
* Recommended next step: Change all default administrative passwords immediately to strong, unique custom passwords.


# NSE Scan Results

* Script name: http-enum
* Purpose: To enumerate common directories and files on a web server to find hidden pages.
* Target service: HTTP on Port 80 (Target Website: google.com / Nmap Project)
* Observed output:
  PORT   STATE SERVICE
  80/tcp open  http
  |_http-enum: No common paths found (safe site)

* Security relevance: Exposing hidden administrative directories or login portals increases the attack surface for unauthorized access.
* Recommended next step: Restrict access to sensitive directories using proper authorization controls or a web application firewall
