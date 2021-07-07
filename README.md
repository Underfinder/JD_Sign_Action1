# 基于github action的京东自动化签到

## 介绍

> 使用NobyDa “京东多合一签到脚本”为基础，移植到github actions自动化执行。


## 触发方式
* 点亮`Star`
* 凌晨0点定时执行
*  自定义：.github/workflows/work.yaml 编辑

## 注意问题

> **问题一：[项目Fork后定时任务没有执行](https://github.com/ZHDeveloper/JD_Sign_Action/issues/3)**
> 
>>1、建议修改README.md提交，以触发定时任务。
>>
>>2、定时任务的时间是UTC时间，跟中国时间有8小时的时差。
> 
>  **问题二：京东Cookie的有效期**
> 
> >就我自己项目中的使用情况而言，一个月有效期。



## 使用用法
* 点击右上角 `Fork` 项目；
* `Settings` -> `Secrets` 中添加京东Cookie、PushPlus token；
	- `JD_COOKIE`：账号1Cookie
	- `JD_DUAL_COOKIE`：账号2Cookie(选填)
	- `PUSH_KEY`：PushPlus SCKEY
* 点击`Star`，任务会自动执行，运行进度和结果可以在`Actions`页面查看；
* 当任务运行完成时，会将运行结果和错误信息打包到`Artifacts`，可自行下载查看；
* 如果配置了：PushPlus，运行结果会推送到微信；

## 获取京东cookie

* 使用项目中的Chrome插件：`JDCookie`；
* Chrome中拓展程序开启`开发者模式`；
* 点击`加载已解压的拓展程序`，选择`JDCookie`目录；
* 登录[领京豆](https://bean.m.jd.com/)；
* 点击`JDCookie`即可拷贝京东cookie；

## 获取PushPlus token

* github 授权登录[PushPlus](http://pushplus.plus/push1.html)官网；
* 菜单栏`微信推送`扫描绑定微信；
* 菜单栏`一对一推送`拷贝token；



## 效果截图

![WechatIMG3](./images/WechatIMG3.jpeg)

![WechatIMG4](./images/WechatIMG4.jpeg)


