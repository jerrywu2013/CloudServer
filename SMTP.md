# SMTP Server Installation Tutorial

#### Install Sendmail
```
sudo apt-get install sendmail
ps aux |grep sendmail
```
#### Setting Sendmail
```
sudo vi /etc/php5/apache2/php.ini
sendmail_path = /usr/sbin/sendmail -i -t
service apache2 restart
```

#### PHP Test mail
```
<?php
$now = date("Y-m-d h:i:s");
$from_name = "Jerry";
$from_email = "jerry@mail.ntust.edu.tw";
$headers = "From: $from_name <$from_email>";
$body = "這是來自".$from_name."<".$from_email.">";
$subject = "[".$now."] 測試信件";


if (mail($from_email, $subject, $body, $headers)) {
echo "success!";
} else {
echo "fail";
}
?>
```
###update "/etc/hosts"
```
IP localhost.localdomain localhost yourhostname
```
