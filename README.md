# Performance Testing 
## Table of Content
- [Introduction](https://github.com/umacb/Performance-Testing-1#introduction)
- [Install](https://github.com/umacb/Performance-Testing-1#install)
- [Prerequisites](https://github.com/umacb/Performance-Testing-1#Prerequisites)
- [Elements of a minimal test plan](https://github.com/umacb/Performance-Testing-1#Elements-of-a-minimal-test-plan)
- [Test Plan](https://github.com/umacb/Performance-Testing-1#Test-Plan)
- [Load Testing Report](https://github.com/umacb/Performance-Testing-1#Load-Testing-Report)
- [Summary Load Testing](https://github.com/umacb/Performance-Testing-1#Summary-Load-Testing)
- [Conclusion](https://github.com/umacb/Performance-Testing-1#Conclusion)
## Introduction
- This report provides an overview of the load testing, stress testing, and spike testing conducted on the test website. The objective of this testing was to evaluate the system's performance under various load conditions and ensure it meets the specified requirements.
## Install
- **Java**  
https://www.oracle.com/java/technologies/downloads/

- **JMeter**  
https://jmeter.apache.org/download_jmeter.cgi     
- =>**apache-jmeter-5.5.zip**

## Prerequisites
- As of JMeter 4.0, Java 8 and above are supported.
- we suggest  multicore CPUs with 4 or more cores.
- Memory 16GB RAM is a good value.

## Elements of a minimal test plan
- Thread Group

    The root element of every test plan. Simulates the (concurrent) users and then runs all requests. Each thread simulates a single user.

- HTTP Request Default (Configuration Element)

- HTTP Request (Sampler)

- Summary Report (Listener)

## Test Plan

Testplan > Add > Threads (Users) > Thread Group (this might vary depending on the JMeter version you are using)
- Name: Thread Group
- Number of Threads (users): 1500
- Ramp-Up Period (in seconds): 100 
- Loop Count: 1  

  1) The general setting for the tests execution, such as whether Thread Groups will run simultaneously or sequentially, is specified in the item called Test Plan.

  2) All HTTP Requests will use some default settings from the HTTP Request, such as the Server IP, Port Number, and Content-Encoding.

  3) Each Thread Group specifies how the HTTP Requests should be carried out. To determine how many concurrent "users" will be simulated, one must first know the number of threads. The number of actions each "user" will perform is determined by the loop count.

  4) The HTTP Header Manager, which allows you to provide the Request Headers that will be utilized by the upcoming HTTP Requests, is the first item in Thread Groups.
 ## Collection of API

-  
    ### List of API 

    - [https://www.restful-booker.herokuapp.com/auth](https://www.restful-booker.herokuapp.com/auth)-Token
    - [https://www.restful-booker.herokuapp.com/booking](https://www.restful-booker.herokuapp.com/booking)-Create Booking
    - [https://www.restful-booker.herokuapp.com/booking/bookingid](https://www.restful-booker.herokuapp.com/booking/bookingid)-Get Booking Info
    - [https://www.restful-booker.herokuapp.com/booking/bookingid](https://www.restful-booker.herokuapp.com/booking/bookingid)-Get Booking Info Update
    - [https://www.restful-booker.herokuapp.com/booking/bookingid](https://www.restful-booker.herokuapp.com/booking/bookingid)-Update Booking
    - [https://www.restful-booker.herokuapp.com/booking/bookingid](https://www.restful-booker.herokuapp.com/booking/bookingid)-Delete Booking
    - 

![image](https://github.com/umacb/CVPR/assets/113898629/266a9135-2e53-4390-b7ae-b678d3ece48e)

## Load Testing Report

![image](https://github.com/umacb/CVPR/assets/113898629/468ae4e4-594b-4e9f-9391-be747a146779)





## Summary Load Testing
- While executing 1500 concurrent requests, 0 requests got connection timeout and the error rate is 0%.
- Server can handle almost concurrent all API calls with almost zero (0) error rate.


## Conclusion
The performance testing conducted on the Opencart website provided valuable insights into the system's behavior and performance under various conditions. Here is a summary of the overall performance testing outcome and the insights gained:

### Summary of Performance Testing Outcome:
- The application demonstrated good performance under normal and expected load conditions.
- Response times were generally within acceptable ranges, meeting user expectations.
- Throughput was satisfactory, handling the expected transaction volume effectively.
- Error rates were low, indicating good application stability and robustness.
### Insights and Observations:
- Scalability Potential: The application exhibited potential for scalability, showing the ability to handle increased load without a significant degradation in performance.

- Database Optimization Opportunities: Analysis revealed areas for optimizing database queries and improving indexing strategies to enhance response times, especially as the user base grows.

- Caching Improvements: Implementing a robust caching mechanism could further optimize response times and reduce the load on the application server.

- Content Delivery Optimization: Leveraging a Content Delivery Network (CDN) for static assets can significantly improve load times for users across different geographic locations.

- Resource Utilization: Monitoring resource utilization during tests highlighted areas where resource allocation could be optimized for better efficiency.

### Recommendations for Improvement:
- Implement a caching strategy to reduce database load and improve response times.
- Conduct a comprehensive database performance tuning exercise to optimize queries and indexing.
- Explore CDN integration to enhance content delivery and reduce latency for users.
- Continuously monitor and optimize resource utilization for optimal system performance.
- The insights gained from this performance testing will serve as a roadmap for optimizing the application's performance, ensuring a seamless and responsive user   experience even during peak load times.

