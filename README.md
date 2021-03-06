# MariaDB CVE Scanner / Patcher 20161104
This script will scan your system for mysql (MariaDB specificly) for [CVE-2016-6663](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-6663) [CVE-2016-6664](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-6664) [CVE-2016-5616](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5616) [CVE-2016-5617](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2016-5617).

**Note**: This script has not been tested with non-mariadb installs

http://www.infoworld.com/article/3138455/security/admins-update-your-databases-to-avoid-the-mysql-bug.html

## usage
From the server you are checking just execute the script passing in the targeted version.
```
./test_database.sh $targeted_version
```

example
```
./test_database.sh "10.1.19-MariaDB"
```

and it will return one of the following

| Return         | Meaning                               |
|----------------|---------------------------------------|
| **Not Intalled | is not installed                      |
| **Current      | version matches `targeted_version`    |
| **Updated      | was updated to the `targeted_version` |
| **FAILED       | attempted to update, but it failed    |
