# Web Application

## Finding software version

* Check source code of the page (Ctrl + u).
* Go through Nmap scan multiple times.
* Research ways to find the version of the software found (sources example: Github pages, documentation pages etc.).

# System enumeration

* `cat .bash_history` to check the history of commands that the user has executed in the Bash shell, might reveal sensitive info.
* For Linux run [linPEAS](https://github.com/peass-ng/PEASS-ng/tree/master/linPEAS) and for Windows run [WinPEAS](https://github.com/peass-ng/PEASS-ng/tree/master/winPEAS). If Windows Defender blocks `Winpeas` try [PrivescCheck](https://github.com/itm4n/PrivescCheck/tree/master).
* Run `ss -lntp`, the command reveals all the services running on the system, including those listening on internal interfaces or bound to loopback addresses.
* If you have read permission for the `.env` file you can use `cat .env` to possibly find some sensitive information.

