# BluesOS Watch Face

vivo watch5 BlueOS 自定义表盘项目。

## 项目结构

```
.
├── package.json           # 项目配置
├── jsconfig.json          # JS 语法校验配置
├── sign/                  # 签名证书目录
│   ├── certificate.pem    # 证书文件
│   └── private.pem        # 私钥文件
└── src/
    ├── app.ux             # 应用入口文件
    ├── manifest.json      # 项目配置（表盘信息、路由、接口声明）
    └── watchface/         # 表盘页面目录
        ├── index.ux       # 表盘主界面
        ├── edit.ux        # 表盘编辑页面
        └── assets/        # 表盘资源文件
            ├── icon.png   # 表盘图标
            └── preview.png # 预览图
```

## 开发环境

- **开发工具**：[BlueOS Studio](https://studio.blueos.com.cn/install)
- **运行时**：Node.js
- **设备**：vivo watch5（圆形表盘，466 x 466 分辨率）

## 开发指南

1. 使用 BlueOS Studio 打开本项目
2. 点击「安装依赖」按钮安装项目依赖
3. 修改 `src/watchface/index.ux` 开发表盘界面
4. 右侧模拟器实时预览效果
5. 完成后点击「打包」生成 rpk 包

## 表盘生命周期

| 事件 | 说明 |
|------|------|
| `onInit` | 表盘初始化，只触发一次 |
| `onReady` | 界面创建完成，只触发一次 |
| `onShow` | 表盘返回前台 |
| `onHide` | 表盘退到后台 |
| `onDestroy` | 表盘退出销毁 |

## 文档参考

- [表盘开发教程](https://developers-watch.vivo.com.cn/reference/extend/watchface/)
- [文件组织](https://developers-watch.vivo.com.cn/reference/configuration/file-organization/)
- [manifest 文件](https://developers-watch.vivo.com.cn/reference/configuration/manifest/)
- [UX 文件](https://developers-watch.vivo.com.cn/reference/configuration/ux-file/)
- [UI 组件](https://developers-watch.vivo.com.cn/component/common/rule/)

## License

MIT
