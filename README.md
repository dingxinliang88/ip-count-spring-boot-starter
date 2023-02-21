# 自定义Starter开发

## 记录系统访客独立IP访问次数

1. 每次访问网站均进行统计
2. 后台每10秒输出一次监控信息（格式：IP + 访问次数）

### 需求分析

1. 数据记录位置：Map / Redis
2. 功能触发位置：每次Web请求（拦截器，网关）
3. 业务参数（配置项）
   1. 输出频度：默认10秒，用户可自定义
   2. 数据特征：累计数据 / 阶段数据，默认是累计数据
   3. 输出格式：详细模式 / 极简模式
4. 校验环境，设置加载条件



### todo

1. 输出到控制台改为输出为文件，以日志的形式输出
2. 加分布式锁 保证线程安全 -- Redission实现
3. 打包上传

