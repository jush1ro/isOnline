isOnline
========

Script for scheduled check of websites availability and mail report. Suited for crontab job.

## Config
1. Configure ```emails.lst``` file and fill it with each email in new line leave an empty line in the end.
2. Configure ```websites.lst``` file and fill it with each website in a new line. leave an empty line in the end.

    Note that the script will follow url(s) with 301 (redirect).

## Add to crontab
Add the following lines to crontab config ($ crontab -e) 

```
THIS_IS_CRON=1
*/5 * * * * cd /path/to/directory/isOnline && ./checker.sh >> api-pqr-stat
```

in this example crontab will run ```checker.sh``` every 5min.

