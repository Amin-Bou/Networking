Here I will showcase how I used NGINX and my personal domain to run a website.

I first bought a domain on Route53 under the domain aminbourenane.com (my personal name).

I then ran an EC2 instance on my AWS account, connecting to it via ssh. This helped me to recap what I have learnt in the Linux module of this course.

I had to assign an A record to my domain in Route53, allowing a connection to my EC2 instance via HTTP: <img width="1616" height="643" alt="image" src="https://github.com/user-attachments/assets/7ae24274-3649-4970-966a-848575fa4728" />

I made sure the security group of my EC2 instance allowed port 80 (HTTP) so that the connection may be successful: <img width="1605" height="241" alt="image" src="https://github.com/user-attachments/assets/3ef643d5-159b-41c5-8568-568a4c11f5d0" />

I then pointed the public IPv4 address of my EC2 instance to the A record of my domain on Route53.<img width="142" height="58" alt="image" src="https://github.com/user-attachments/assets/8c9ed046-e26c-465a-aae8-1fa99755067c" />

I tested that everything was functional by using the 'sudo systemctl status nginx' command to ensure NGINX was running properly. I then copied and pasted the domian I bought from Route53 into my browser to find that it was working: <img width="1910" height="398" alt="image" src="https://github.com/user-attachments/assets/4d66bfe3-3934-40ed-88aa-1911b715edf0" />

(I noticed that each time I restarted the instance, I needed to change the value in my A record as the IP kept on changing, next time I should use an IP to avoid this mistake)

