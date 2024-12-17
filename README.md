# Catch2_model
According to Catch2 official website `https://github.com/catchorg/Catch2`, write a use case

# 版本选择

![image-20241216165611233](./assets/image-20241216165611233.png)

根据版本推荐,我们使用Catch2的v2.x版本

我们将Catch2作为子模块,所以,

你在克隆本项目时,除了要执行`git clone git@github.com:1AoB/Catch2_model.git`,

```bash
你还需要执行
cd Catch2_model/  
git submodule update --init --recursive
来初始化子模块Catch2的v2.x版本.
```

（库中的Catch2库就是我从官方的v2.x版本自编译）

# Excellent Git training opportunity!

Below, I will write:

How to use the v2.x version of Catch2 library as a submodule for this project:

1. cd Catch2_model
2. git submodule add https://github.com/catchorg/Catch2.git Catch2   此时会生成子模块的配置文件.gitmodules
3. cd Catch2
4. git checkout v2.x   此时再去上传就是v2.x这个版本了
5. cd .. 
6. git add Catch2
7. git commit -m "Added Catch2 submodule locked to v2.x branch"

但是我发现这种方式不是很靠谱,经常因为网络原因只可以加载主模块,但是不可以加载子模块.



# 想让catch2运行起来需要配置：

1.添加头文件 ../../Catch2/include

2.添加宏定义 CATCH_CONFIG_MAIN

