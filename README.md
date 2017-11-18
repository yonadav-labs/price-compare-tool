
## BBSW
This is a django project and web project so there is no need to compile deploy.

##### Steps to deploy:

- Git clone the source code
```
git clone <repo>
```

 
- Register download cron

When you deploy to /root
 
```
*/10 * * * * python /root/Appeagle_scrape_price_strategy_compare/download_reports.py
```
Here you can change the interval. Now it is 10 minutes

- Launch the site

```
cd /root/Appeagle_scrape_price_strategy_compare
nohup python manage.py runserver 0.0.0.0:80 < /dev/null &
```