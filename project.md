## Docemantation on configuration of apache as a loadbalancer

1. Lauch Ec2 Ubuntu-server and open TcP port 80 as a loadbalancer

2. Install apache2 on Websercer


`sudo apt install apache2 -y`

`sudo apt-get install libxml2-dev`

3. Enable following modules

`sudo a2enmod rewrite`

`sudo a2enmod proxy`

`sudo a2enmod proxy_balancer`

`sudo a2enmod proxy_http`

`sudo a2enmod headers`

`sudo a2enmod lbmethod_bytraffic`

- Configure load balancing

`sudo vi /etc/apache2/sites-available/000-default.conf`

`sudo tail -f /var/log/httpd/access_log`

- Open this file on your LB server

`sudo vi /etc/hosts`

`sudo systemctl restart apache2`






