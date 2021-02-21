## 基本配置修改

>[!TIP|label:步骤：]

> 打开configuration.yaml，我们按需修改：
> ```
> homeassistant:
  #经纬度
  latitude: 38.455
  longitude: 115.3633
  #海拔
  elevation: 30
  #度量单位，默认米
  unit_system: metric
  #时区
  time_zone: Asia/Shanghai
  #系统昵称，显示在主界面顶部
  name: Home
> ```

## 加入路由器

```
# 加入路由器
device_tracker:
  - platform: xiaomi
      host: 192.168.31.1 
      username: 123456789
      track_new_devices: yes
```

## 开启设备追踪

```
# 开启设备追踪
device_tracker:
  - platform: nmap_tracker
      hosts: 192.168.31.1/24
      home_interval: 10   # 每十秒ping一次
      consider_home: 30  # 30秒 ping不同 就认为离家
```

## 将 Node-Red 加入侧边栏

```
# 将 Node-Red 加入侧边栏
panel_iframe:
node_red:
  title: node_red
  icon: mdi:vector-polyline
  url: [url]http://192.168.31.69:1880/[/url]
```



