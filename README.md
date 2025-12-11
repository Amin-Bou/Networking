Here I will showcase how I used NGINX and my personal domain to run a website.

I first bought a domain on Route53 under the domain aminbourenane.com (my personal name).

I then ran an EC2 instance on my AWS account, connecting to it via ssh. This helped me to recap what I have learnt in the Linux module of this course.

I had to assign an A record to my domain in Route53, allowing a connection to my EC2 instance via HTTP.

I made sure the security group of my EC2 instance allowed port 80 (HTTP) so that the connection may be successful.

I then pointed the public IPv4 address of my EC2 instance to the A record of my domain on Route53.

I tested that everything was functional by using the 'sudo systemctl status nginx' command to ensure NGINX was running properly. I then copied and pasted the public IP of my EC2 instance into my browser to find that it was working.
