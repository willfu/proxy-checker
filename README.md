proxy-checker
It will

crawl proxies from www.coobobo.com, cn-proxy.com, kxdaili.com, 881free.com, haoip.cc, , ip3366.net, www.66ip.cn.
the free proxies of www.goubanjia.com and www.kuaidaili.com are always unavailable, they are removed.
you can also add other proxy website as you like.
check proxies availability
figure out their type
TRANSPARENT_PROXY
ANONYMOUS_PROXY
DISTORTING_PROXY
HIGHANONYMITYPROXY
output proxies in squid format
Generally, you will get around ~500 avaiable proxies, which contain ~200 high anonymity proxies.
usage
mvn clean -Dmaven.test.skip packge

run crawler & checker client

only run crawler(which doesn't need checker server)
java -jar proxy-checker-client-1.0-SNAPSHOT.jar -a crawl

only run checker(which need checker server) java -jar proxy-checker-client-1.0-SNAPSHOT.jar -a check -s http://[checker-server-ip]:8080/proxy-check

run them both java -jar proxy-checker-client-1.0-SNAPSHOT.jar -a all -s http://[checker-server-ip]:8080/proxy-check

deploy checker server on any machine which has public ip

java -jar proxy-checker-server-1.0-SNAPSHOT.jar