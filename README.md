# Rails Engine 组件

## 组件列表


* [rails_org](https://github.com/work-design/rails_org): 组织架构、基础 OA 功能、同时实现了 SaaS 系统基础；
* [rails_trade](https://github.com/work-design/rails_trade): 处理电商，主要处理订单、支付（支付宝、微信支付、Paypal、Stripe、苹果支付）、促销
* [rails_vip](https://github.com/work-design/rails_vip): 会员
* [rails_event](https://github.com/work-design/rails_event): 预约系统，处理 时间、地点、参与者（主持人、普通参与者）
* [rails_crm](https://github.com/work-design/rails_crm): 客户关系(CRM)
* [rails_enquiry](https://github.com/work-design/rails_enquiry): 询价系统, 待开发完善
* []

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