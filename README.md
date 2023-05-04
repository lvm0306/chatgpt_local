
# chatgpt api版部署

标签（空格分隔）： 未分类

---

### 默认大家已有的知识
1.docker安装
2.chatgpt账号注册
3.可以用github

### 一、获取api-key

1.登录 [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) 输入chatgpt账号

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683188849436-6fb4e777-2dae-4053-847c-92c3a9d8e148.png#averageHue=%23fefefe&clientId=u305db602-5f90-4&from=paste&height=625&id=udfbe7a1a&originHeight=625&originWidth=1375&originalType=binary&ratio=1&rotation=0&showTitle=false&size=91029&status=done&style=none&taskId=u0596051b-028e-44c3-acf6-35a006e600f&title=&width=1375)

点击create 后记得保存好 sk开头的一个字符串
到此api-key 获取完毕

### 二、docker拉取镜像

```
docker pull chenzhaoyu94/chatgpt-web
```
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683189281344-98354f0f-3ea0-4543-948d-7f181d0b8f79.png#averageHue=%23f0f0f2&clientId=u305db602-5f90-4&from=paste&height=215&id=u96a74a87&originHeight=215&originWidth=1169&originalType=binary&ratio=1&rotation=0&showTitle=false&size=17853&status=done&style=none&taskId=ubf6dabd7-4753-4f76-a505-29c6439df4f&title=&width=1169)

![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683189390025-2ad84f15-ba53-4e70-a44b-342dbeaaf631.png#averageHue=%23fcf9f9&clientId=u305db602-5f90-4&from=paste&height=735&id=ue7ca5f86&originHeight=735&originWidth=705&originalType=binary&ratio=1&rotation=0&showTitle=false&size=76884&status=done&style=none&taskId=u25b0be00-9659-4538-8b10-0bf32c6669a&title=&width=705)
运行起来后 打开localhost:3002
应该会进入到本地化chatgpt ui
现在启动docker 的这个机器 只要能链接到 google就可以了
现在已经实现了，本地局域网都可以通过 ip+port的方式 使用chatgpt-api版本，但是外网是访问不到的，下一步是如何外网访问到 这台设备
### 三、外部访问
推荐natapp
[传送门](https://natapp.cn/) 没有的话快速注册一个
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683189732539-21dd6d88-dd67-467e-a63b-8f382da5749c.png#averageHue=%23fbfaf8&clientId=u305db602-5f90-4&from=paste&height=428&id=u094d4d95&originHeight=428&originWidth=729&originalType=binary&ratio=1&rotation=0&showTitle=false&size=136067&status=done&style=none&taskId=ucfd470cc-f09f-40cd-80fb-2ec64021977&title=&width=729)
选择vip1型就可以
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683189858383-08a15814-5359-4c76-8289-7da211135591.png#averageHue=%23f4f3f1&clientId=u305db602-5f90-4&from=paste&height=591&id=uf5d228ba&originHeight=591&originWidth=1341&originalType=binary&ratio=1&rotation=0&showTitle=false&size=320194&status=done&style=none&taskId=u0cab2a7f-140a-4bf3-a019-24fb9a72e86&title=&width=1341)
> 优惠码C958717B


![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683190037268-c35369de-0d0f-49c5-8d95-1ccd430c36d5.png#averageHue=%23faf7f6&clientId=u305db602-5f90-4&from=paste&height=812&id=u921e387f&originHeight=812&originWidth=1360&originalType=binary&ratio=1&rotation=0&showTitle=false&size=153120&status=done&style=none&taskId=ue5b7b786-a47d-4031-ba96-f74a61f924f&title=&width=1360)
付费完成后
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683190171905-244beaa2-47ee-41a5-ae6e-610b10ba5df0.png#averageHue=%23f9f7f4&clientId=u305db602-5f90-4&from=paste&height=85&id=uf9a3c7cf&originHeight=85&originWidth=1565&originalType=binary&ratio=1&rotation=0&showTitle=false&size=86949&status=done&style=none&taskId=u78c75d34-6521-4e87-a6c1-0b9db9144e3&title=&width=1565)
![image.png](https://cdn.nlark.com/yuque/0/2023/png/21552416/1683190229534-423d12de-eaa5-4385-aa1c-b43cc2e755d3.png#averageHue=%23fdfbfb&clientId=u305db602-5f90-4&from=paste&height=776&id=u06bfb173&originHeight=776&originWidth=1258&originalType=binary&ratio=1&rotation=0&showTitle=false&size=75011&status=done&style=none&taskId=ufafda498-9997-43ff-971b-91da81b85b4&title=&width=1258)
现在就可以 通过 你的 xxx.natapp1.cc 网站 访问到 你的chatgpt-web  页面了
除了docker 的部署方式 还有其他的部署方式
传送门 [https://github.com/Chanzhaoyu/chatgpt-web](https://github.com/Chanzhaoyu/chatgpt-web)
也可以直接部署到本地




