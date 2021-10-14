# 美团限时抢红包 天天神券 脚本 #
## 支持功能 ##
### 一.每日自动签到领美团豆(可兑换红包必中符),每日可领七次 ###
### 二.每日自动抢天天神券(开放时间北京时间11点,17点,21点) ###
### 三.自动将抢到的面值小于5元的天天神券兑换成红包豆(如满17-3面值的) ###
### 四.自动遍历红包库和道具库 ###
### 五.自动查询豆子详情 ###
### 六.接入第三方微信推送平台 ###
# 使用说明 #
## 将脚本部署在服务器或者github action等可读写文件的云平台上,本脚本只在服务器上测试通过。若需在腾讯云函数平台请自行修改源码中参数，否则无法运行在腾讯云函数等无法读取文件的云函数平台！！！！##
# #
## 首次执行脚本需按提示输入参数，后续即可自动读取脚本所在目录的配置文件 ##
# **即设置crontab等定时计划前一定要手动运行一遍脚本记录token等参数 ！！** #
## 本脚本接入server 酱微信推送 ,为节约每天免费5条的推送额度，故本脚本将只在早上11点后进行消息推送 ## 

[![image.png](https://img30.360buyimg.com/pop/jfs/t1/211928/18/400/3186526/61684712Ef5ec3a67/cd3d1ce86fede2f9.png)](https://img30.360buyimg.com/pop/jfs/t1/211928/18/400/3186526/61684712Ef5ec3a67/cd3d1ce86fede2f9.png)
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/212555/4/392/2725735/616846a5E8f351912/07fef1b4b64bfb3a.png)](https://img30.360buyimg.com/pop/jfs/t1/212555/4/392/2725735/616846a5E8f351912/07fef1b4b64bfb3a.png)
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/202198/14/11250/1607299/616846caE26c3154c/5d068ac30952a3e1.png)](https://img30.360buyimg.com/pop/jfs/t1/202198/14/11250/1607299/616846caE26c3154c/5d068ac30952a3e1.png)
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/6778/24/17726/1739591/61684609E2ad8c9ed/a93d66149466a7ea.png)](https://img30.360buyimg.com/pop/jfs/t1/6778/24/17726/1739591/61684609E2ad8c9ed/a93d66149466a7ea.png)

[![image.png](https://img30.360buyimg.com/pop/jfs/t1/207193/40/5418/1291762/61684639Ebaec599d/fd29ae22c87c7473.png)](https://img30.360buyimg.com/pop/jfs/t1/207193/40/5418/1291762/61684639Ebaec599d/fd29ae22c87c7473.png)
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/168607/17/21165/1958061/61684654E8df975ae/37655de02096bf0c.png)](https://img30.360buyimg.com/pop/jfs/t1/168607/17/21165/1958061/61684654E8df975ae/37655de02096bf0c.png)
[![image.png](https://img30.360buyimg.com/pop/jfs/t1/215836/35/357/1348513/6168466fE8ef70adc/9bd7013ff4ce2202.png)](https://img30.360buyimg.com/pop/jfs/t1/215836/35/357/1348513/6168466fE8ef70adc/9bd7013ff4ce2202.png)