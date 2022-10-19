# 工程简介

基于flowable 6.7.2 的 flowable ui扩展工程，为方便系统集成将官方ui模块独立出来，方便绘制流程图及系统扩展

# 使用

1. 克隆或下载项目
2. 修改 resource下的application.properties文件，将数据源切换为自己的

![image-20221019180648185](F:\hugo\flowable-ui-extend\README.assets\image-20221019180648185.png)

3. 修改账号密码

![image-20221019180716604](F:\hugo\flowable-ui-extend\README.assets\image-20221019180716604.png)

4. 启动后访问

`http://localhost:9090/flowable-ui/#/`

默认账户密码：admin/test

![image-20221019180734383](F:\hugo\flowable-ui-extend\README.assets\image-20221019180734383.png)

默认集成了

admin（管理）、idm（身份认证）、modeler（建模）、task(任务)模块，如不需要相关模块请删除pom文件中的相关starter，请尽量保证基本的idm和modeler模块

![image-20221019180748651](F:\hugo\flowable-ui-extend\README.assets\image-20221019180748651.png)

# 人员、组或角色集成（可选）

系统启动完成后会自动创建数据表，将自己系统中的用户、组或者角色集成到下面表中

![image-20221019180800777](F:\hugo\flowable-ui-extend\README.assets\image-20221019180800777.png)

即可在画流程图的时候选择到相关人员、组或者角色

| 表                | 说明                                                         |
| ----------------- | ------------------------------------------------------------ |
| act_id_user       | 用户表                                                       |
| act_id_group      | 组表，不想用组可以把自己系统中的角色同步过来是一样的，组和角色叫法不一样，本质上使用起来差不多 |
| act_id_membership | 用户和组的关联关系表，组里放的是角色的话可以理解为角色用户关联表 |

![image-20221019180810868](F:\hugo\flowable-ui-extend\README.assets\image-20221019180810868.png)

