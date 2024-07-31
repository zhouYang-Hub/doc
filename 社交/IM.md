#### IM

- [ ] <font color='red'>生产环境 group_members 新增 字段 group_type， 生产环境上线需要刷数据</font>

- [ ] s_system_message 新增字段 

  

增加角色，修改角色，废除角色 （一个车队最多有两个副车队长 、一个安全员）

​	群类型  1.车队群  2.线路群 3.货运单群 4.车队管理群

​	角色类型 1:观察员；2 ：安全员 ；3 车队长结算专员 ；  4: 副车队长 

极光推送 ：

processor_id=1008, job_id=88, action_id=-9999999, 

INFO  - [10:18:22.161][HTTP.JSONP]【==> 收到接口请求-数据原型】: processor_id=1008, job_id=88, action_id=-9999999, token=null, new_data={"typeu":52,"dataContent":"{\"isJpush\":0,\"sourceUserId\":4166615951853043452,\"businessType\":1,\"m\":\"{\\\"msg_content\\\":\\\"{\\\\\\\"contain\\\\\\\":\\\\\\\"请下载合伙人APP，并使用账号18999999999并使用收到的验证码完成登录\\\\\\\",\\\\\\\"action\\\\\\\":\\\\\\\"captain_assignment_truck\\\\\\\",\\\\\\\"captain\\\\\\\":\\\\\\\"高慧鹏\\\\\\\",\\\\\\\"title\\\\\\\":\\\\\\\"恭喜你成为安全员\\\\\\\"}\\\",\\\"msg_type\\\":0}\"}"}, old_data=null, format=null, jsoncallback=null | (MyControllerJSONP^recieveFromClient:377)



```json
1016-24-51  管理员群修改职务
1016-24-48  移除/废除职务
```

```json
{
    "isJpush":0,
    "sourceUserId":4166615951853043452,
    "businessType":1,
    "m":"{msg_content:"contain":"请下载合伙人APP，并使用账号18999999999并使用收到的验证码完成登录","action":"captain_assignment_truck","captain":"高慧鹏","title":"恭喜你成为安全员,"msg_type":0}
}
```





```
private Integer businessTypeCode;
private String businessTypeContent;

private BusinessTypeEnum(Integer businessTypeCode, String businessTypeContent) {
    this.businessTypeCode = businessTypeCode;
    this.businessTypeContent = businessTypeContent;
}

public Integer getBusinessTypeCode() {
    return this.businessTypeCode;
}

public String getBusinessTypeContent() {
    return this.businessTypeContent;
}
```
