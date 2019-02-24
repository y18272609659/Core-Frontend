# 繁盛王国

版本：0.01 (000)。

# 部署

```bash
### Frontend
# install dependencies
npm install

# copy `config/index.js.bac` to `config/index.js`, update your index.js::proxyTable.host:
# on cros, the test server to accept port is 8080 or 8081
#     proxyTable: {
#           '/': {
#             target: 'http://www.nice-kingdom.uio',
#             changeOrigin: true,
#           }
#         },

# Serve with hot reload at localhost:8080 or other tips
npm run dev

# Build for production with minification
npm run build

# Build for production and view the bundle analyzer report
npm run build --report

# If you want auto build & publish, run it:
./sh build
```

# 相关

## 外部工具

文档：[NiceKingdom - ShowDoc](https://www.showdoc.cc/testnk?page_id=1090320475297537)

原型：[NiceKingdom - XiaoPiu](https://www.xiaopiu.com/project?proid=5c6e991492a6615e8baf21ca)

## 开发

前端遵循 ESLint 检查器定义的规则，需要变通的地方，请提 Issue 讨论。

# 许可（LICENSE）

本项目（NiceKingdom 核心模块的服务端部分）遵循 [MPL 2.0 开源许可证](https://github.com/NiceKingdom/Core-Frontend/blob/master/LICENSE)。
NiceKingdom/Core-Frontend is [MPL 2.0 licensed](https://github.com/NiceKingdom/Core-Frontend/blob/master/LICENSE).

