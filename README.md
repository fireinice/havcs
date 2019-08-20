# 备注
- 请仔细阅读[介绍及使用说明](https://ljr.im/articles/plugin-smart-speaker-access-home-assistant-integration/)
- 注意检查HA日志插件是否成功启动
- 使用过程中有疑问请加QQ群307773400交流。
- 本分支为最新的开发版本，旧版本到[releases页面](https://github.com/cnk700i/aihome/releases)下载

# 更新日志
- 2019-08-20
  1. 小度音箱支持light、switch、inputboolean类型定时打开/关闭指令，需配合common_timer插件使用。
- 2019-05-10
  1. 采用新方案，在不影响HA的token超时时间参数情况下，现在可以为token独立设置超时时间
- 2019-05-07
  1. 修复原生input_boolean打开关闭指令失效
  2. 修复token正则匹配不正确
- 2019-05-06
  1. 重新设计配置项更容易设置
  2. 优化三种模式代码逻辑
  3. 整合模式一服务网关，重新测试
  4. 优化调试日志的样式
- 2019-05-03
  1. input_boolean实体支持对调节亮度操作指令映射service（aihome_actions属性）
  2. 指令映射模式下，支持执行多条指令（设置方法有变化，请查看教程）
  2. HA 0.92.1版本测试
- 2019-04-09
  1. 增加设备配置样例（使用packages方式导入即可测试）
  2. 修复叮咚启动不同步信息bug
- 2019-04-07
  1. 精简配置项，增加模式三简略配置说明
- 2019-04-01
  1. 增加首次启动连接mqtt测试功能，如果正常INFO级别日志会显示提示信息，否则请检查appkey以及网络连接
- 2019-03-29
  1. 设备开关状态主动上报（小度音箱），可通过配置文件设置是否上报
  2. HA 0.90.2版本测试
  3. 前端页面优化，上线了密码找回功能
- 2019-03-06
  1. HA 0.88.2版本测试
- 2019-02-27
  1. input_boolean支持直接调用service指令
- 2019-02-22
  1. 增加叮咚设备更新（插件启动触发更新）
  2. 修复京东音箱、小度音箱对input_boolean类的开/关控制
  3. 天猫精灵设备配置命名风格统一
  4. 更改设备发现模式为非主动发现,使用"aihome_device"属性设置设备可被发现
  5. 传感器类设备配置属性精简
  6. 说明文档补充设备配置样例
- 2019-01-xx
  HA 0.86.4 和 HA 0.82.1，本地单机测试

# 调试
插件无法工作可设置插件日志debug级别以观察调试消息。
```yaml
# {HA配置目录}/configuration.yaml
logger:
  default: info
  logs:
    custom_components.aihome: debug
```
