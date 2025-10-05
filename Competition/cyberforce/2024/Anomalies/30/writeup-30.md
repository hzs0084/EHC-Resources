# Questions

## Identify all User Agents involved in accessing or attempting to access phpmyadmin or phpMyAdmin.

Command used: cat logs.txt | grep -e "phpmyadmin" -e "phpMyAdmin" 

Output: 2024-09-27 07:45:31 - 192.0.2.202 ==> PROXY-XYZ [FW-ACCEPT] [RULE-107] - - [2024-09-27 07:45:31 +0000] "GET /phpmyadmin HTTP/2" 200 722 "BreezeFlow Navigator" "User-Agent: MidnightIndexer/4.5.7 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.159 Safari/537.36" SNORT-ALERT: [SID:1000077; RULE: PhpMyAdmin Access Attempt; content:"/phpmyadmin";]
2024-09-27 08:00:55 - 198.51.100.189 ==> PROXY-XYZ [FW-ACCEPT] [RULE-108] - - [2024-09-27 08:00:55 +0000] "GET /phpMyAdmin HTTP/2" 404 2328 "TurbineWise Analytics" "User-Agent: MidnightIndexer/4.5.7 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.159 Safari/537.36" SNORT-ALERT: [SID:1000078; RULE: PhpMyAdmin Access Attempt (capital); content:"/phpMyAdmin";]


Answer:  User-Agent: MidnightIndexer/4.5.7

## What is the full timestamp and IP address associated with the last SQL injection attempt targeting controlsystem/gl4c/admin? (YYYY-MM-DD hh:mm format)

Command Used: cat logs.txt | grep -e "controlsystem/gl4c/admin"

Output: 2024-09-27 07:58:49 - 192.0.2.237 ==> PROXY-XYZ [FW-ACCEPT] [RULE-115] - - [2024-09-27 07:58:49 +0000] "GET /controlsystem/gl4c/admin?user=1' OR '1'='1'-- HTTP/2" 500 2453 "WindStream Optimizer" "User-Agent: TuskTracker/4.5.1 (Macintosh; Intel Mac OS X 10_13_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.181 Safari/537.36" SNORT-ALERT: [SID:1000152; RULE: SQL Injection via Admin Query; content:"/controlsystem/gl4c/admin?user=1' OR '1'='1'--";]
2024-09-27 10:58:52 - 192.0.2.237 ==> PROXY-XYZ [FW-ACCEPT] [RULE-110] - - [2024-09-27 10:58:52 +0000] "POST /controlsystem/gl4c/admin/password_reset HTTP/2" 404 5300 "WindStream Optimizer" "User-Agent: TuskTracker/4.5.1 (Macintosh; Intel Mac OS X 10_13_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.181 Safari/537.36" SNORT-ALERT: [SID:1000135; RULE: Password Reset Access Attempt; content:"/controlsystem/gl4c/admin/password_reset";]
2024-09-27 11:33:14 - 192.0.2.202 ==> PROXY-XYZ [FW-ACCEPT] [RULE-104] - - [2024-09-27 11:33:14 +0000] "POST /controlsystem/gl4c/admin/password_reset HTTP/2" 403 1527 "BreezeFlow Navigator" "User-Agent: MidnightIndexer/4.5.7 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.159 Safari/537.36" SNORT-ALERT: [SID:1000135; RULE: Password Reset Access Attempt; content:"/controlsystem/gl4c/admin/password_reset";]
2024-09-27 12:16:47 - 198.51.100.202 ==> PROXY-XYZ [FW-ACCEPT] [RULE-100] - - [2024-09-27 12:16:47 +0000] "POST /controlsystem/gl4c/admin/password_reset HTTP/2" 404 5798 "GaleNet Portal" "User-Agent: FerretScanner/6.4.9 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Edge/16.16299" SNORT-ALERT: [SID:1000135; RULE: Password Reset Access Attempt; content:"/controlsystem/gl4c/admin/password_reset";]


Answer: Timestamp and IP addr

2024-09-27 07:58:49 - 192.0.2.237

## Which IP addresses attempted to access the file path /.git/config?


Command Used: cat logs.txt | grep -e "/.git/config"            


Output: 2024-09-27 08:08:52 - 203.0.113.146 ==> PROXY-XYZ [FW-ACCEPT] [RULE-118] - - [2024-09-27 08:08:52 +0000] "GET /.git/config HTTP/2" 200 256 "GaleNet Portal" "User-Agent: MidnightIndexer/4.5.7 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.4515.159 Safari/537.36" SNORT-ALERT: [SID:1000085; RULE: Git Config Access; content:"/.git/config";]


Answer: 203.0.113.146

## What is the User Agent associated with a successful access (returned a 200) of the .env file for the BreezeFlow Navigator application?


I hope you get the idea, need to figure these answers out eventually, moving on to another anomaly for now




