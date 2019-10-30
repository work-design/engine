# engine
check which engine has changed

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