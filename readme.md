# 美团限时抢红包 天天神券 脚本 #
[![followers](https://img.shields.io/badge/dynamic/json?color=%09%2300BFFF&label=Github&prefix=followers%3A&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3DfuguiKz)](https://img.shields.io/badge/dynamic/json?color=%09%2300BFFF&label=Github&prefix=followers%3A&query=%24.data.totalSubs&url=https%3A%2F%2Fapi.spencerwoo.com%2Fsubstats%2F%3Fsource%3Dgithub%26queryKey%3DfuguiKz)
[![author:fugui](https://img.shields.io/badge/author-fuguiKz-brightgreen)](https://img.shields.io/badge/author-fuguiKz-brightgreen)
[![MIT](https://img.shields.io/badge/license-MIT-brightgreen)](https://img.shields.io/badge/license-MIT-brightgreen)
## 求star 求关注 拒绝白嫖 呜呜呜  ##
[![6af89bc8gw1f8q48ds6y9g205k046aas.gif](https://img30.360buyimg.com/pop/jfs/t1/206851/38/5699/37222/616ae4e0E962e8669/c497dffab436fec1.gif)](https://img30.360buyimg.com/pop/jfs/t1/206851/38/5699/37222/616ae4e0E962e8669/c497dffab436fec1.gif)
# #
### 之前所有旧版本都存在重大逻辑问题，新版本已修复，请不要使用旧版
###
## 支持功能 ##
### 一.每日自动签到领美团豆(可兑换红包必中符),每日可领七次 ###
### 二.每日自动抢天天神券(道具库中若有任意面值必中符，则自动在设置的时间段使用。抢红包开放时间为北京时间11点,17点,21点) ###
### 三.自动将抢到的面值小于5元的天天神券兑换成红包豆(如满17-3面值的) ###
### 四.自动遍历红包库和道具库 ###
### 五.自动查询豆子详情 ###
### 六.接入第三方微信推送平台 [pushPlus](https://www.pushPlus.plus) 和[server酱](https://sct.ftqq.com/) ###
### 七.自动查询红包池红包🧧详情  ###
# #
## 新增[pushPlus](https://www.pushPlus.plus) 推送 ##
###  此推送每天限额200次 对比server酱每天5次的免费推送，推荐使用pushPlus ###
# #
### [pushPlus](https://www.pushPlus.plus) 与[server酱](https://sct.ftqq.com/)默认使用的推送接口目前虽可继续使用，但已被微信宣告放弃,默认推送接口停止服务时间待定，故请尽量更改推送接口,采用企业微信机器人推送 ###
### [企业微信机器人webhook获取方式](https://juejin.cn/post/6844903887212642312) ###
# #
### 建议pushPlus和server酱推送均使用企业微信机器人推送渠道，需下载企业微信，申请机器人记住webhook,pushPlus需**按照下图在脚本开头**填写webhook 地址，server酱webhook地址不用填在脚本里，只需在server 酱网页端选择推送渠道并填写即可 ###
# #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/217881/11/615/215705/616ab2ebEa559bfe6/e32d58baeeded5ae.png)](https://img30.360buyimg.com/pop/jfs/t1/217881/11/615/215705/616ab2ebEa559bfe6/e32d58baeeded5ae.png)
# # 
## 新增自定义时间段执行尝试领30元以上红包功能 ##
# #
### 对尝试以下领取30元以上红包功能自定义时间段(**在有10元以上必中符的情况下，现默认为下午和晚上两个时间段之间自动尝试抢大额**)，即在设置的时间段内，且有10元以上必中符，才会尝试领取30元以上红包，否则在其他时间段会直接使用必中符抢红包，不会尝试去等15元以上红包领完才去抢。 ###
### 自定义大额时间段如下图所示 一般不建议改动 ###
# #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/212624/29/723/592014/616b89b2Efddefce7/94aa61d96e93380d.png)](https://img30.360buyimg.com/pop/jfs/t1/212624/29/723/592014/616b89b2Efddefce7/94aa61d96e93380d.png)
# #
## 新增尝试领取30元以上红包功能 ##
# #
### 一、当道具库拥有10元以上面值必中符时(若想用红包豆领到限量的15元必中符，则需在脚本第一次初始化变量时将propId填为5,每天三点准时运行一遍脚本),自动尝试等待红包池中15元被清空后领取30元以上红包，小概率成功事件 ###
# #
### 二、5元和8元红包由于数量过大，无法利用红包数量近似性领取更高层级的红包 ###
# #
### 三、若想运行时默认关闭此新增功能，请将五十五行(如下图)的连续赋值变量从1改为0即可 ###
# #
### 四、若在有10元以上必中符且在自定义抢红包时间段内，自动尝试领取30元以上红包时，出现无法领取到任何红包的情况，则请将下图中 ten_left fifteen_left 数值改大些，如改成10左右 ###
# #
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/198361/27/13260/202683/616988e0Edf077ba8/e2db2244bc9c9def.png)](https://img30.360buyimg.com/pop/jfs/t1/198361/27/13260/202683/616988e0Edf077ba8/e2db2244bc9c9def.png)
# #
## 使用说明 ##
### 将脚本部署在服务器或者nas openwrt 或者潘多拉路由器 群晖等可读写文件的平台上,本脚本只在服务器上测试通过。若需在腾讯云函数平台请自行修改源码中参数，否则无法运行在腾讯云函数等无法读取文件的云函数平台 ###
# #
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

### linux，windows，android，路由器openwrt，nas等任何设备只要有Python3环境和终端即可运行。 ###
# #
## 模块要求 ##
### python3基本不需要安装任何模块  直接尝试运行脚本,要是缺哪个模块就安哪个 ###

# #
## 定时计划设置 ##
### 假设脚本文件存放在 testUser用户的主目录 /testUser 目录下 ###
### **Linux平台(包括openwrt 等路由器 nas 群晖设备)定时计划命令** ###
### *crontab -l*  ###
###   *crontab -e*  ###
###   *选择你会用的终编辑器，如vim等*  ###
### 若需 每天11点、14点、17点、21点、0点后的一个小时内的0分，1分，32分运行一次脚本,则可按如下设置 ###
# #
### 14点为运行美团豆兑换必中符时间段，0,1,2,3点为补充每天的签到领红包豆次数，其他时间段为抢红包时间段! ###
# #
![image.png](https://img30.360buyimg.com/pop/jfs/t1/215764/28/426/39105/6168d739E5d72d02e/b4e3e96aebd87543.png)
###   0 11,14,17,21,0,1,2,3 *  *  * /usr/bin/env python3  /testUser/meituanshenquan.py ###
# #
### crontab 配置如下图 ###
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/168797/30/24833/58700/616b985bEb25c7864/40d606d2fed21371.png)](https://img30.360buyimg.com/pop/jfs/t1/168797/30/24833/58700/616b985bEb25c7864/40d606d2fed21371.png)
# #
### **windows平台设置定时任务计划** ###
## 参考[Windows创建计划任务定时执行Python脚本](https://cloud.tencent.com/developer/news/295826)此篇文章 ###

## docker 使用提示 ##
###  个人觉得docker是个**伪需求**，套娃python3 环境个人觉得没必要，这个项目又不是用js写的，对环境要求没那么高，若真想使用docker 直接构建一个python3的docker就行或者自己构建个alpine或者ubuntu的docker去装python3，下图为dockerhub的python3镜像，按描述构建后，然后docker exec -it docker的名字 /bin/bash  进入docker 然后安装git, 再git clone  此项目源码，其他的运行和定时任务就和linux实体机一样了 ### 
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/199060/30/13635/365840/616bf9d5Ef8061804/144729685f84dff9.png)](https://img30.360buyimg.com/pop/jfs/t1/199060/30/13635/365840/616bf9d5Ef8061804/144729685f84dff9.png)
### 很多人真是为了docker 而docker ，pull个镜像遇到网不好直接卡半天，**用docker 的一般都是nas 或者openwrt ，自己实体机装个python3很难吗？** ###
# #
### *至于腾讯云函数和github action,由于个人学业和时间问题，很抱歉的宣告放弃支持，那么没有服务器，电脑，nas,openwrt路由器这些设备就没办法运行了python脚本了吗？注意是python 脚本，当然安卓手机也是能运行的啦，装个termux,termux装python3 就能运行脚本了，什么，你说上面所有的设备都没有，那建议就不要用了* ###
#  #


## 注意事项 ##
### 定时计划时**不要使用输出重定向** 脚本自动生成的output.txt 起到记录推送的功能 每次内容会自动覆盖，所以**执行时不要使用任何输出重定向命令**!!!!!!!!!! ###
# #
## 欢迎访问[个人博客](https://armbian.icu) ##



 ###  ###
## 脚本运行后推送server 酱效果展示: ##

[![image.png](https://img30.360buyimg.com/pop/jfs/t1/206801/36/5447/3928857/61691181E0e80bb5f/ed30b59e9084d572.png)](https://img30.360buyimg.com/pop/jfs/t1/206801/36/5447/3928857/61691181E0e80bb5f/ed30b59e9084d572.png)
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