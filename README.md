### 渠道SDK接口

#### 域名
&emsp;&emsp;测试域名:`sdk-test-api.lezhonggame.com` <br/>
&emsp;&emsp;正式域名:`lzapi.lezhonggame.com`

#### 请求方式
&emsp;&emsp;**POST**

#### 加密方式
&emsp;&emsp;1.除sign以外的参数，以键排序，值做urlencode 然后按下面示例拼串 <br/>
&emsp;&emsp;2.对上面字符串进行md5加密 <br/>
&emsp;&emsp;3.加密KEY:***<br/>

#### 登录
&emsp;&emsp;链接：`https://域名/login/chlLogin/getAccount` <br/>
&emsp;&emsp;参数：`channel_pkg_num`    &emsp;&emsp;&emsp;&emsp;    渠道包ID  <br/>
&emsp;&emsp;&emsp;&emsp;&emsp;`info`   &emsp;&emsp;&emsp;&emsp;             设备信息   示例：{"device_id":"fb9eec7f-6df7-2019-af5e-7ad7dfefd593", "device_model":"EVR-AL00", "mac":"74:ac:5f:9e:9f:bb", "bundle":"com.admin.tom", "version":"1.0.1"}<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;`tokenkey` &emsp;&emsp;&emsp;&emsp;          小七渠道账号值   <br/>
&emsp;&emsp;&emsp;&emsp;&emsp;`time` &emsp;&emsp;&emsp;&emsp;          时间戳   <br/>
&emsp;&emsp;&emsp;&emsp;&emsp;`sign` &emsp;&emsp;&emsp;&emsp;          sign验签值 <br/>
 
