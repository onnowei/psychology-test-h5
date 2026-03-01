# 育儿心理测试H5

一款基于MBTI理论的儿童性格测试H5应用，帮助家长了解孩子的性格特点，获得个性化育儿建议。

## 功能特性

- 🧠 **MBTI性格测试** - 20道专业题目，科学评估孩子性格
- 📊 **详细分析报告** - 16种性格类型解析
- 💡 **个性化育儿建议** - 根据性格类型提供针对性建议
- 💰 **付费解锁报告** - 完整版16页专业报告
- 📱 **微信分享** - 支持分享到微信好友和朋友圈

## 技术栈

### 前端
- 原生HTML5 + CSS3 + JavaScript
- 响应式设计，适配移动端
- 无需构建工具，直接部署

### 后端
- Node.js + Express
- RESTful API
- 内存存储（可扩展至MongoDB）

## 快速开始

### 1. 安装依赖

```bash
# 后端
cd backend
npm install

# 前端（可选，用于本地预览）
cd ../frontend
npm install
```

### 2. 启动服务

```bash
# 启动后端（端口3000）
cd backend
npm start

# 前端直接打开 index.html 或使用静态服务器
# 方式1：直接打开文件
open ../frontend/index.html

# 方式2：使用静态服务器
cd ../frontend
npx serve .
```

### 3. 访问应用

- H5页面: http://localhost:3000
- API文档: http://localhost:3000/api/health

## API接口

| 接口 | 方法 | 说明 |
|------|------|------|
| /api/health | GET | 健康检查 |
| /api/results | POST | 保存测试结果 |
| /api/results/:id | GET | 获取测试结果 |
| /api/payment/create | POST | 创建支付订单 |
| /api/payment/status/:orderId | GET | 查询支付状态 |
| /api/stats | GET | 获取统计数据 |

## 项目结构

```
ai-product-assistant/
├── frontend/          # H5前端
│   ├── index.html    # 主页面
│   ├── styles.css    # 样式文件
│   ├── app.js        # 应用逻辑
│   └── package.json
├── backend/          # 后端服务
│   ├── server.js     # Express服务器
│   └── package.json
└── README.md
```

## 部署说明

### 前端部署
1. 将 `frontend/` 目录内容上传至静态服务器（如CDN、OSS）
2. 或使用 Vercel/Netlify 一键部署

### 后端部署
1. 使用 PM2 启动服务：`pm2 start server.js`
2. 配置 Nginx 反向代理
3. 配置域名和SSL证书

### 微信支付接入
1. 注册微信支付商户号
2. 配置支付回调URL
3. 替换 `app.js` 中的支付逻辑

## 后续优化

- [ ] 接入真实微信支付API
- [ ] 添加用户登录和测试历史
- [ ] 实现海报生成功能
- [ ] 添加数据统计看板
- [ ] 接入数据库持久化存储
- [ ] 添加更多测试类型（天赋、 parenting风格等）

## 许可证

MIT
