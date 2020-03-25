# Rails Engine 组件

## 组件列表

* [rails_com](https://github.com/work-design/rails_com)：基础通用 engine，对 Rails 框架进行了一些扩展
* [rails_auth](https://github.com/work-design/rails_auth)：用户系统，支持多账号、多设备登陆，支持第三方登陆；
* [rails_role](https://github.com/work-design/rails_role)：权限系统，支持多个维度，如 SaaS 系统中，某个组织是否开通某个功能；
* [rails_org](https://github.com/work-design/rails_org)：组织架构、基础 OA 功能、同时实现了 SaaS 系统基础；
* [rails_trade](https://github.com/work-design/rails_trade)：处理电商，主要处理订单、支付（支付宝、微信支付、Paypal、Stripe、苹果支付）、促销
* [rails_vip](https://github.com/work-design/rails_vip)：会员
* [rails_event](https://github.com/work-design/rails_event)：预约系统，处理 时间、地点、参与者（主持人、普通参与者）
* [rails_crm](https://github.com/work-design/rails_crm)： 客户关系(CRM)
* [rails_enquiry](https://github.com/work-design/rails_enquiry)：询价系统, 待开发完善
* [rails_agency](https://github.com/work-design/rails_anency)：代理人体系，代理人受客户委托，获得权限，在系统进行对应操作
* [rails_attend](https://github.com/work-design/rails_attend)：出席、出勤、缺勤
* [rails_audit](https://github.com/work-design/rails_audit)：审计、审批，对于系统里变更的数据，可以通过审计日志恢复；
* [rails_bench](https://github.com/work-design/rails_bench)：项目、任务、流水线；
* [rails_data](https://github.com/work-design/rails_data)：数据导入、数据导出，并可生成图表；
* [rails_detail](https://github.com/work-design/rails_detail)：对某个模型的细节描述，元数据处理分析；
* [rails_doc](https://github.com/work-design/rails_doc)：能直接从 Rails 应用的代码分析给出 Api 文档；
* [rails_factory](https://github.com/work-design/rails_factory)：生产管理系统：原材料入厂、组装加工、出厂；
* [rails_finance](https://github.com/work-design/rails_finance)：财务管理：报销，预支等；
* [rails_growth](https://github.com/work-design/rails_growth)：黑客增长
* [rails_interact](https://github.com/work-design/rails_interact)：用户评论、点赞、收藏等互动性质的交互；
* [rails_log](https://github.com/work-design/rails_log)：错误日志记录并发送通知(企业微信、飞书)，邮件发送记录，CSP 内容安全日志；
* [rails_notice](https://github.com/work-design/rails_notice)：通告、通知系统，高性能；
* [rails_profile](https://github.com/work-design/rails_profile)：用户信息，生日、地址等通用信息处理；
* [rails_ship](https://github.com/work-design/rails_ship)：电商系统中的发货管理；
* [rails_wait](https://github.com/work-design/rails_wait)：预约排队功能；
* [rails_sync](https://github.com/work-design/rails_sync)：新老系统进行数据同步迁移、支持多种关系型数据库(Mysql / Postgresql)
* [rails_wechat](https://github.com/work-design/rails_wechat)：微信公众号、企业微信、小程序综合对接应用，支持微信通知、菜单等各种功能，支持 SaaS 体系；

## 使用

更新子模块(engine)

* 第一次初始化项目
```
git submodule update --init
```

* 后续更新项目
```
git submodule update --rebase
git submodule update --merge 
```

* 更新每个engine(子项目)
```shell
git submodule update --init --recursive
git submodule update --rebase --recursive
```

## engine 加载顺序
在gemfile靠后的engine的model常量会先加载； 