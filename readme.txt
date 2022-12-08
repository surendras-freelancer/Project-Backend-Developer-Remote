Login Details

Admin User
username - admin@example.com
password - MyPassword


Other User
username - test@example.com
password - MyPassword

Login Page:
http://127.0.0.1:8000/

Home Page:
http://127.0.0.1:8000/

For Cron / Rabbitmq (Add/Update News article)
1) First run the below command on screen for continous running ( for read messages/queue)

php bin/console rabbitmq:consumer messaging

2) Add below cron to start queue after every 10 minute(for start queue)

*/10 * * * *  /usr/bin/curl http://127.0.0.1:8000/send-message/1

3) Create database with news_auth and then upload Database.sql


