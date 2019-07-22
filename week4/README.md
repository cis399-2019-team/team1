## Week 4 Deliverables

### 1. URLs and foo.html

    Homepages:
    http://34.212.149.129/
    http://34.209.30.19/

    Foo.html can be accessed by adding "foo.html" trailing either url.

### 2.  Access log

    ubuntu@ip-10-0-1-84:/var/log/apache2$ sudo less access.log
    24.20.207.204 - - [22/Jul/2019:20:31:18 +0000] "GET / HTTP/1.1" 200 446 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:68.0) Gecko/20100101 Firefox/68.0"
    10.0.1.105 - - [22/Jul/2019:21:00:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:01:04 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:01:18 +0000] "GET /favicon.ico HTTP/1.1" 404 542 "-" "Mozilla/5.0 (Windows NT 10.0; Win64;      x64; rv:68.0) Gecko/20100101 Firefox/68.0"
    10.0.1.105 - - [22/Jul/2019:21:01:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:02:04 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:02:10 +0000] "-" 408 0 "-" "-"
    10.0.1.105 - - [22/Jul/2019:21:02:10 +0000] "-" 408 0 "-" "-"
    10.0.1.105 - - [22/Jul/2019:21:02:15 +0000] "-" 408 0 "-" "-"
    10.0.1.105 - - [22/Jul/2019:21:02:15 +0000] "-" 408 0 "-" "-"
    10.0.1.223 - - [22/Jul/2019:21:02:30 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:02:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:05:00 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:05:04 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:05:30 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:05:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:06:00 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"

### 3. Domain name of the load balancer

    http://team1balancer-79271232.us-west-2.elb.amazonaws.com/

### 4. Load balancer tests

    Shutting down one instance causes a moment that, when accessing the web server, a blank page is returned. The server returns the correct html file when the page is refreshed after a second or two. 

    Shutting down both instances causes the load balancer to return only blank page.

    After rebooting the instances, the load balancer takes significantly more time to start up than simply accessing the domain without the associated load balancer.

### 5. Load balancer health checks and access logs

    Keir
    -----------------------------------------------------------------------------------
    10.0.1.223 - - [22/Jul/2019:21:02:30 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:02:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:05:00 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:05:04 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:05:30 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.105 - - [22/Jul/2019:21:05:34 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"
    10.0.1.223 - - [22/Jul/2019:21:06:00 +0000] "GET /index.html HTTP/1.1" 200 425 "-" "ELB-HealthChecker/1.0"

    -----------------------------------------------------------------------------------
    Adrian
    -----------------------------------------------------------------------------------
    -----------------------------------------------------------------------------------

### 6. Puppet code
   
    The Puppet source code can be found at https://github.com/cis399-2019-team/team1-puppet

    The Apache2 module can be found in "code/modules" 
