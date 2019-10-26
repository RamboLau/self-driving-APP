## 项目结构

``` bash

│  
├── main.js # 入口JS文件
│    
├── uni.scss  # 公共样式
│ 
├── App.vue    # 根组件
│ 
├── api
│   └── ...    # 抽取出API请求
├── static
│   └── ...    # 存放应用引用静态资源（如图片、视频等）的地方，注意：静态资源只能存放于此
├── libs
│   └── ...    # 插件封装
├── components  # 基础组件
│   └── ...    
├── pages      # 业务页面文件存放的目录
│   └── ...    
├── filters    # 全局过滤器
│   └── ...
├── common     # 公共资源
│   └── uni.scss    # 全局样式
└── store
    └── ...    # 状态管理
```