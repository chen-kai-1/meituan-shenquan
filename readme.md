# 美团限时抢红包 天天神券 脚本 #
## 支持功能 ##
### 一.每日自动签到领美团豆(可兑换红包必中符),每日可领七次 ###
### 二.每日自动抢天天神券(开放时间北京时间11点,17点,21点) ###
### 三.自动将抢到的面值小于5元的天天神券兑换成红包豆(如满17-3面值的) ###
### 四.自动遍历红包库和道具库 ###
### 五.自动查询豆子详情 ###
### 六.接入第三方微信推送平台 ###
# #
## 使用说明 ##
### 将脚本部署在服务器或者github action等可读写文件的云平台上,本脚本只在服务器上测试通过。若需在腾讯云函数平台请自行修改源码中参数，否则无法运行在腾讯云函数等无法读取文件的云函数平台!!! ##
# #
### 首次执行脚本需按提示输入参数，后续即可自动读取脚本所在目录的配置文件 ###
## **即设置crontab等定时计划前一定要手动运行一遍脚本记录token等参数 ！！** ##
### 本脚本接入server 酱微信推送 ,为节约每天免费5条的推送额度，故本脚本将只在早上11点后进行消息推送 ### 
# #
## 美团token获取方法 ##
### 获取token的方式:百度搜[美团](https://www.meituan.com/)，若谷歌浏览器登陆网页版美团若登录时的异常验证提交点不动，请更换safari等其他浏览器尝试即可.登录后在美团首页F12检查，点击network，刷新网页，拖进度条点击第一个请求，然后复制请求头中cookie 的token字段，注意只要token字段，格式为"token={token};"中的{token}字段，不带分号，更不是整个cookie。
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/204166/23/11541/512124/6168cea1Ef1540fe6/de62fb75e02d62c8.png)](https://img30.360buyimg.com/pop/jfs/t1/204166/23/11541/512124/6168cea1Ef1540fe6/de62fb75e02d62c8.png)
### 或者使用浏览器插件 [editthiscookie](https://www.editthiscookie.com/) 也可快速获得token字段 ###
# #
## 脚本兼容性解答 ##

### linux，windows，android，路由器openwrt，nas等只要有Python3环境和终端即可运行。github action 理论能运行，腾讯云函数这种不能新建和读取文件的云函数平台暂不支持。 ###
# #
## 依赖导入方法 ##
### 需事先安装好脚本头部声明的依赖文件 可通过在终端，进入对应的脚本存放位置，执行命令自动安装依赖的模块(此自动安装模块中声明的依赖版本仅在python3.8测试过，若安装依赖失败，请手动参考脚本头文件声明的依赖手动导入,不指定版本)
*pip install -r requirement.txt*
###
# #
## 定时计划设置 ##
### 假设脚本文件存放在 testUser用户的主目录 /testUser 目录下 ###
### **Linux平台(包括openwrt 等路由器 nas 群晖设备)定时计划命令** ###
### *crontab -l*  ###
###   *crontab -e*  ###
###   *选择你会用的终编辑器，如vim等*  ###
### 若需 每天11点、17点、21点、0点后的一个小时内的0分，1分，32分运行一次脚本，则可按如下设置 ###
![image.png](https://img30.360buyimg.com/pop/jfs/t1/215764/28/426/39105/6168d739E5d72d02e/b4e3e96aebd87543.png)
###   0,1,32 11,17,21,0 *  *  * /usr/bin/env python3  /testUser/meituanshenquan.py ###

### **windows平台设置定时任务计划** ###
## 参考[Windows创建计划任务定时执行Python脚本](https://cloud.tencent.com/developer/news/295826)此篇文章 ###

## 注意事项 ##
### 定时计划时**不要使用输出重定向** 脚本自动生成的output.txt 起到记录推送的功能 每次内容会自动覆盖，所以**执行时不要使用任何输出重定向命令**!!!!!!!!!! ###
# #
### 欢迎访问[个人博客](https://armbian.icu) ###



 ###  ###
## 脚本运行后推送server 酱效果展示: ##

[![image.png](https://img30.360buyimg.com/pop/jfs/t1/211928/18/400/3186526/61684712Ef5ec3a67/cd3d1ce86fede2f9.png)](https://img30.360buyimg.com/pop/jfs/t1/211928/18/400/3186526/61684712Ef5ec3a67/cd3d1ce86fede2f9.png)
 #  #

 ### 天天神券活动页面展示  ###
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/212555/4/392/2725735/616846a5E8f351912/07fef1b4b64bfb3a.png)](https://img30.360buyimg.com/pop/jfs/t1/212555/4/392/2725735/616846a5E8f351912/07fef1b4b64bfb3a.png)
 # #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/202198/14/11250/1607299/616846caE26c3154c/5d068ac30952a3e1.png)](https://img30.360buyimg.com/pop/jfs/t1/202198/14/11250/1607299/616846caE26c3154c/5d068ac30952a3e1.png)
 # #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/6778/24/17726/1739591/61684609E2ad8c9ed/a93d66149466a7ea.png)](https://img30.360buyimg.com/pop/jfs/t1/6778/24/17726/1739591/61684609E2ad8c9ed/a93d66149466a7ea.png)
 # #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/207193/40/5418/1291762/61684639Ebaec599d/fd29ae22c87c7473.png)](https://img30.360buyimg.com/pop/jfs/t1/207193/40/5418/1291762/61684639Ebaec599d/fd29ae22c87c7473.png)
 # #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/168607/17/21165/1958061/61684654E8df975ae/37655de02096bf0c.png)](https://img30.360buyimg.com/pop/jfs/t1/168607/17/21165/1958061/61684654E8df975ae/37655de02096bf0c.png)
 # #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/215836/35/357/1348513/6168466fE8ef70adc/9bd7013ff4ce2202.png)](https://img30.360buyimg.com/pop/jfs/t1/215836/35/357/1348513/6168466fE8ef70adc/9bd7013ff4ce2202.png)
 # #