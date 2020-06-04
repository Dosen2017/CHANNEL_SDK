### 渠道SDK接口

#### 域名
&emsp;&emsp;测试域名:`sdk-test-api.lezhonggame.com` <br/>
&emsp;&emsp;正式域名:`lzapi.lezhonggame.com`

#### 请求方式
&emsp;&emsp;**POST**

#### 加密方式
&emsp;&emsp;1.除sign以外的参数，以键排序，值做urlencode 然后按下面示例拼串 <br/>
&emsp;&emsp;&emsp;&emsp;示例：channel_pkg_num=880010402&password=999999&time=1523728323&user_name=Aa144e235skks&KEY<br/>
&emsp;&emsp;2.对上面字符串进行md5加密 <br/>
&emsp;&emsp;3.加密KEY:*** <br/>

#### 登录
&emsp;&emsp;链接：`https://域名/login/chlLogin/getAccount` <br/>
&emsp;&emsp;参数：<br/>
&emsp;&emsp;&emsp;&emsp;1.公共参数：
 | 参数名   |      参数规格      | 必填   |      说明      |
 |----------|:-------------:|:-------------:|:-------------:|
 | channel_pkg_num |  int |  Y |  渠道ID |
 | os |  int |  Y |  系统：1.IOS,2.安卓 |
 | info |  int |  Y |  设备信息 示例：{"device_id":"fb9eec7f-6df7-2019-af5e-7ad7dfefd593", "device_model":"EVR-AL00", "mac":"74:ac:5f:9e:9f:bb", "bundle":"com.admin.tom", "version":"1.0.1", "b_id":"hss_12aa"}|
 | time |  int |  Y |  当前时间 |
 | sign |  string |  Y |  签名 |
 
 info字段说明：<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;device_id :设备ID<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;device_model : 设备模型<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;mac : MAC<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;bundle : 包ID<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;version : 工程版本号<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;b_id : 包标识（非母包的安卓需要传入）<br/>
 
&emsp;&emsp;&emsp;&emsp;2.渠道参数： 
 | 参数名   |      参数规格      | 必填   |      说明      |
 |----------|:-------------:|:-------------:|:-------------:|
 | tokenkey |  string |  Y |  小七token值 |

#### 充值
##### 小七充值
&emsp;&emsp;&emsp;&emsp;1.game_sign接口
| 参数名   |      参数规格      | 必填   |      说明      |
 |----------|:-------------:|:-------------:|:-------------:|
 | extends_info_data |  string |  Y |  扩展参数 |
 | game_area |  string |  Y |  角色所在游戏区 |
 | game_level |  string |  Y | 用户游戏中角色等级 |
 | game_orderid |  string |  Y |  游戏订单号 |
 | game_price |  string |  Y |  商品价格（使用元为单位） |
 | game_role_id |  string |  Y |  用户游戏中角色 ID 信息 |
 | game_role_name |  string |  Y |  用户游戏中角色名称 |
 | game_guid |  string |  Y |  标识用户在小 7 平台中的唯一标识 |
 | notify_id |  string |  Y |  回调通知的 id |
 | subject |  string |  Y |  道具简介 |
 | time |  int |  Y |  当前时间 |
 | sign |  string |  Y |  签名 |
