## Prometheus配置的热加载
Prometheus配置信息的热加载有两种方式：

- 第一种热加载方式：查看Prometheus的进程id，发送SIGHUP信号:

``` shell
kill -HUP <pid>
```

- 第二种热加载方式：发送一个POST请求到/-/reload，需要在启动时给定--web.enable-lifecycle选项：

```shell
 curl -X POST http://localhost:9090/-/reload
```

## 重启prometheus
netstat -nap | grep 9090   #查看prometheus 的进程id 

kill -9 PID    #关闭prometheus 的进程

./prometheus --config.file=./prometheus.yml    #重启prometheus  


## consul
cd consul.d/
配置client.json
nohup ./consul agent --config-dir=consul.d/ &



