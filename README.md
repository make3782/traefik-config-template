# traefik-config-template
traefik配置文件一些注释与demo,基于traefik V2,使用Yaml格式

### 使用
- 下载traefik 2.x版本到当前目录
- 启动
```
./traefik --configfile=./traefik.yaml
```

### 测试目的
- 使用`file`动态配置
- 使用`consul catlog`方式动态加载

### Tips
- `access log`不知道动态切割, 官方建议使用`logrotate`自行处理 😓
- `access log`是全局配置,不想nginx一样可以根据不同域名配置日志到不同文件,就是所有来源的请求都在一个文件里,自己`logstash`处理 😓
- `consul`通过服务加载,我这边测试会有延时,不像`file`的方式马上可以生效