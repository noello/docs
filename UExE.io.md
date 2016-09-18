以一个典型的物联网业务举例：
一个wifi空调：
参与角色：目的：交互媒介：业务内容
空调厂商：运营：MCS/浏览器：应用统计，OTA，售后报修管理等
最终用户：使用空调：iOS/Adnroid：连接空调上网，控制空调，收集空调状态等
MCS：运营：MCS：计费

从开发者视角，以用户发出一次空调控制命令的过程来看，开发者要在什么地方做哪些开发：
1. 总体：规划控制命令协议
2. 设备端：用js实现这个控制交互
3. iOS/Adnroid：用H5实现这个控制交互
4. MCS：用node.js实现对这个控制交互的统计数据收集和计费
5. MCS WEB FRONTEND:用H5实现这个控制交互的统计数据收集和计费的view

一个完整的业务，被分段，在不同的地方去各自实现。跨语言，跨系统，跨知识背景。
弊端：周期长，人力要求复杂

设想一个平台叫UExE.io: Unified Engine for vairious Envioranment, 由cloud web IDE+unified js automatice-deploying runtime on various Environment（node.js, ML.js, iOS/Adnroid, MCS）组成，在cloud web IDE中以业务为视角，进行一次总体开发，提交后IDE自动分发至相关环境的runtime中，各环境中runtime根据统一的framework运行属于自己的任务。
