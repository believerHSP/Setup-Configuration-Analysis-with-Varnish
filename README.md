# Setup-Configuration-Analysis-with-Varnish
It involves setting up Varnish in a containerized environment, configuring access logs for monitoring, and analyzing the response time in backend request calls.

# how to decide the mount point on any container: what are parameters kept in mind while figuring it out??

# Http server: https://www.docker.com/blog/how-to-use-the-apache-httpd-docker-official-image/ 
        https://www3.ntu.edu.sg/home/ehchua/programming/howto/Apache_HowToConfigure.html#:~:text=Listen%3A%20to%20bind%20Apache%20to,to%20check%20the%20existing%20connections).
        

# 1. Running a Varnish container: varnish-software.com/developers/tutorials/running-varnish-docker/ 

1. We advise you to install Varnish Cache 6.0 LTS, which is a stable and supported version.
2. The varnish:stable and varnish:6.0 tags refer to Varnish Cache 6.0 LTS
3. 

# 2. Enabling logs: https://docs.varnish-software.com/tutorials/enabling-logging-with-varnishncsa/






# 27/12/2023
                                                                                  Ref-Link: https://docs.varnish-software.com/tutorials/enabling-logging-with-varnishncsa/
1. rc.local file needs to be created at /etc path.
2. Add this command:  varnishncsa -a -w /var/log/varnish/access.log -D -P /var/run/varnishncsa.pid -F '%h %l %u %t "%r" %s %b "%{Referer}i" "%{User-agent}i" %D'
3. Execute the above command will create a access.log file automatically in the /var/log/varnish/ path.
4. restart the container.
7. then try curl localhost:ContainerIP And see the access.log file.

8. How to redirect it to STDOUT, so that I could see it via podman logs command.
9. 



# 28/12/2023
                        Steps in developing Custom Dockerfile
   
1. 




















