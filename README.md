# Rails Engine 组件

## [组件列表](https://work.design/price)


## 新增一个组件

* 从 0 开始新增一个 engine:
  * `rails plugin new --full rails_xxx`
  * 进入 rails_xxx 目录
    * `git init`
    * `git submodule add git@github.com:work-design/dummy.git test/dummy`
* 在 .gitmodules 加入配置信息：
  1. `git submodule add git@github.com:work-design/rails_xxx.git rails_xxx`
  2. `git submodule absorbgitdirs rails_xxx`

* 进入 rails_xxx, 执行 git checkout master

## 使用

更新子模块(engine)

* 第一次初始化项目
```
git clone git@github.com:work-design/engine.git
git submodule update --init
git submodule foreach git checkout main
```

* 后续更新项目
```
git pull
git submodule update --rebase(或--merge) 
```

* 更新每个engine(子项目)
```shell
git submodule update --init --recursive
git submodule update --rebase --recursive
```

## engine 加载顺序
在gemfile靠后的engine的model常量会先加载； 


## 其他
bundle config local.rails_xxx ~/your_main_project_path/engine_path/rails_xxx

BUNDLE_DISABLE_LOCAL_BRANCH_CHECK: "true"

