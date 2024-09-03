# 💎 原生Three 和 Cesium 案例 - 更新到死 - 只做开源 -

##  开源不易 - ⭐ - 点星助力

加入仓库一起管理 联系🐧QQ             |  🐧QQ群         
:-------------------------:|:-------------------------:
2586300277  |  865182188  

- github dev分支实时预览 http://z2586300277.github.io/three-cesium-examples
  
- vercel 部署预览 https://three-cesium-examples.vercel.app
  
- 友情链接3D编辑器 https://github.com/z2586300277/three-editor
  
- 注: 点个星星，不管遇到任何技术艰难险阻，three-cesium-examples 永远站在你身后。

## 📦 自行部署

1.可通过 config/links 文件修改 所有的链接和 logo, 替换成自己的官网或者链接地址。

2.如在 http://threehub.cn/ 部署

## 🌳创作

##### - 如果这些里面有案例帮助了您 - 有意的话您可以提交您的作品 - 让爱传递给更多开发者

##### - fork仓库后 - 增加用户信息 - 上传您最自豪的作品 - 提交合并到主分支 - 开发或者合并 基于dev分支

- 运行框架  启动服务端口指向index.html即可

1. 创作者可以在 config/author.js 录入你的开发者信息,然后你提交的案例关联上id 就会展示作者信息。

2. 将案例js放入目录cesiumExamples/threeExamples 中的文件夹中 如threeExamples/basic中放入 test.js, test.jpg, 或者目录test[test.js, test.jpg]

3. 在config目录下 找到threeExamples 录入案例信息, 内部的资源指向与你的 js 和 image 资源路径对应

4. 注: 为保证轻量化 案例展示图片资源使用 - https://yasuo.xunjiepdf.com/img/  _(自定义压缩至4k以内)_

5. 涉及其他依赖js,可将module.js 放到js目录  如 dat.gui,gasp ,注入方式 config.js 可见

6. 音视频模型存储等一些可以公用的资源 files 文件夹下,涉及文件资源尽量引用外部url

- config  js注入和配置案例信息目录
- files 音视频模型存储等一些可以公用的资源, 尽量不要上传文件资源, 使用 外部url 地址访问
- js => dat.gui gsap 等等一些依赖存放处,尽量可使用线上依赖引入
- threeExamples three.js 案例代码目录
- cesiumExamples cesium 案例代码目录

```js
// HOST 自动获取 当前域名/ip 防止部署环境不同 资源引用失效
{
    id: '父级列表唯一id',
    name: '名称',
    author: '作者id',
    image: HOST + 'threeExamples/basic/test.jpg', // 对应窗口图
    codeUrl: HOST + 'threeExamples/basic/test.js', // js module格式 大多数案例形式
    htmlUrl: HOST + 'threeExamples/test/test.html' // html 在线格式 如 three案例 => 粒子 => 随机粒子 粒子行星
    openUrl: '预览外联地址url', // openurl 和 codeurl 为二选一形式 如 可见桃花亭 su7 案例
    downloadUrl: '附带下载的url', // 如three.js => 高级案例 => 桃花亭
    githubUrl: '附带github 仓库的url', // 如 three.js => 开源作品 => su7
    meta: {
        title: '此案例网站标题',
        keywords: '搜索引擎关键字',
        description: '此案例页面描述'
    }
}
```

## 🏠 搭建自己的分布式存储仓库

- 架构设计是以请求资源形式访问代码,所以如 codeUrl image, 等资源信息不局限于存储在 本仓库中，例如存储在你自己的服务器，然后url 访问到你的资源地址即可。

- 然后在此仓库仅配置 案例信息即可, 可参考 three案例 => 扩展功能 => 3D 地图 案例的配置

- 注 由于 github 访问限制 http 会被自动禁止, 建议 也搭建自己得github page ,使用 github 充当自己的资源服务器。

- 如：我的一些分布式资源存储在 https://github.com/z2586300277/3d-file-server 仓库下 —— 访问服务: https://z2586300277.github.io/3d-file-server/

- github page 搭建  => 创建仓库 => 页面流程 => setting => pages => Build and deployment => source (depoly from a branch) => branch 选择对应分支

- 注： github page 搭建完成后 直接访问 如 https://xxxx.github.io/xxxx/ 下的资源文件无法显示是正常现象, 在代码中可正常获取

- 参考访问案例 如 cesium 案例 => 离线地图 => 内网高德
