# Before Installation
Build a PHP Environment. If you use CentOS 7,
```
# yum -y install httpd php
```

# Installation
```
# cd /var/www/html
# mkdir json_receiver
# cd json_receiver
# git https://github.com/KunioHayakawa/json_receiver.git
```

# Post a request
```
# curl -X POST http://localhost/json_receiver/json_receiver.php -d '{ "name":"Kunipon", "age":"20"}'
```

# Check the Web Server's error log
```
# tail -n 1 /var/log/httpd/error_log
(You7ll see below.)
[Mon Jun 29 23:21:04.745913 2020] [:error] [pid 2202] [client ::1:36608] { "name":"Kunipon", "age":"20"}
```
