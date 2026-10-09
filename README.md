# clash-
在国外，连很多为国内用户准备的机场延迟很高或者连不上  
连热点
<img width="1881" height="1012" alt="image" src="https://github.com/user-attachments/assets/66facadd-2da5-41c3-8ca2-17f6ea5e5ccc" />
<img width="1836" height="1232" alt="image" src="https://github.com/user-attachments/assets/3b96923d-a0ef-4589-8cdf-a04c12498b1d" />
<img width="1878" height="1250" alt="image" src="https://github.com/user-attachments/assets/4cb44ddc-ffdd-4805-b9bf-58d95cd28d27" />


---
连校园网的情况更差，不知道是我这个大学的校园网ip被识别为垃圾ip了还是怎么
<img width="1901" height="1026" alt="image" src="https://github.com/user-attachments/assets/17fe051e-abf3-4c5c-9ca6-1fbf27465f98" />

# clash在linux系统上的杂乱问题
搞了好几小时linux上的代理问题了，奇奇怪怪。
我目前是用的这个https://github.com/nelvko/clash-for-linux-install

```
curl -sS -o /dev/null -w "http_code=%{http_code}\n" --max-time 15 https://www.google.com
curl: (28) Failed to connect to www.google.com port 443 after 7714 ms: Connection timed out
http_code=000
```
这样说明还没开启linux上的clash

```
curl -sS -o /dev/null -w "http_code=%{http_code}\n" --max-time 15 https://www.google.com
curl: (35) OpenSSL SSL_connect: Connection reset by peer in connection to www.google.com:443 
http_code=000
```
这样说明这个节点服务器有问题。


···
curl -sS -o /dev/null -w "http_code=%{http_code}\n" --max-time 15 https://www.google.com
http_code=200
···
这样说明linux上的clash代理和节点的连接顺利运行了
