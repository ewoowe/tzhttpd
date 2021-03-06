### TZHTTPD
This is a high-performance while easy-to-be-used HTTP service framework, which can help you develop a HTTP-featured server quickly.   

### Key Points of TZHTTPD
1. Developed with Boost.Asio, which means high-concurrency with high-performance. Very poor virtual machine can support up to 1.5K QPS, so I believe it can satisfy performance requirements in most cases.    
2. Just supporting HTTP GET/POST methods, but feed the need of most backend application gateway development. Parameters and post body are well handled and structed. Routing handlers based on uri regex-match.    
3. Connection can be keep-alived, and automatically timed out and be removed.   
4. Support loading handlers through .so library, this feature simulates legacy CGI deployment conveniently. This library try its best loading and updating handler with less impact for others.    
5. Based on Boost library and C++0x standard, so can used in legacy but widely-deploied RHEL-6.x environment.   
6. Not buggy, and has stood tests in a way.    

### Possible usage
1. General Web server, KIDDING. TZHTTPD does not support full HTTP protocal, so it may not behave well in this situation.   
2. Backend application gateway, YES. TZHTTPD is designed and optimized for this purpose.   
3. HTTP protocal adaptor. This way TZHTTPD can be use as proxy, it accept and parse HTTP request, forward the request and transform corresponding respose as standard HTTP response.   
4. Service manage interface. You can integrate TZHTTPD into your already project, then you can send customize uri to interfere your service, such as configuration update, runtime statistic output, ...   

### Performance
![siege](siege.png?raw=true "siege")

### Reference project   
[tzmonitor](https://github.com/taozhijiang/tzmonitor).   
