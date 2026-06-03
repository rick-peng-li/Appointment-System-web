# 预约管理系统 (Appointment-System-web)

> 项目 Git 地址：`[请填写实际的 Git 仓库地址]`

## 项目简介

这是一个基于 React + Node.js 的在线预约管理系统，主要用于医院或诊所的医生预约场景。系统支持用户注册登录、浏览医生列表、预约挂号、医生管理等功能。

## 技术架构

### 前端技术栈
- **框架**: React 18
- **构建工具**: Vite
- **状态管理**: Redux Toolkit
- **路由**: React Router
- **UI 样式**: TailwindCSS 3 + 自定义 CSS

### 后端技术栈
- **框架**: Node.js + Express
- **数据库**: MongoDB
- **认证**: JWT (JSON Web Token)
- **密码加密**: bcryptjs

## 项目结构

```
Appointment-System-web/
├── client/                 # 前端代码
│   ├── public/             # 静态资源
│   ├── src/
│   │   ├── components/     # 公共组件
│   │   ├── pages/          # 页面组件
│   │   ├── redux/          # Redux 状态管理
│   │   ├── styles/         # 样式文件
│   │   ├── Data/           # 模拟数据
│   │   └── assets/         # 资源文件
│   ├── index.html          # HTML 入口
│   ├── main.jsx            # React 入口
│   └── vite.config.js      # Vite 配置
├── config/                 # 配置文件
│   └── db.js               # 数据库连接配置
├── controllers/            # 控制器
│   ├── userController.js   # 用户控制器
│   ├── doctorController.js # 医生控制器
│   └── adminController.js  # 管理员控制器
├── models/                 # 数据模型
│   ├── userModels.js       # 用户模型
│   ├── doctorModel.js      # 医生模型
│   └── appointmentModel.js # 预约模型
├── routes/                 # 路由配置
│   ├── userRoutes.js       # 用户路由
│   ├── doctorRoutes.js     # 医生路由
│   └── adminRoutes.js      # 管理员路由
├── middlewares/            # 中间件
│   └── authMiddleware.js   # 认证中间件
├── server.js               # 服务端入口
└── package.json            # 项目依赖配置
```

## 功能特性

### 用户功能
- 用户注册与登录
- 浏览医生列表
- 预约挂号
- 查看个人预约记录
- 接收系统通知

### 医生功能
- 医生注册申请
- 查看个人资料
- 管理预约信息

### 管理员功能
- 用户管理
- 医生管理
- 审核医生申请

## 快速开始

### 环境要求
- Node.js >= 16.x
- MongoDB >= 4.x
- npm >= 8.x

### 安装依赖

```bash
# 安装后端依赖
npm install

# 安装前端依赖
cd client
npm install
```

### 配置环境变量

在项目根目录创建 `.env` 文件：

```env
PORT=8080
MONGO_URI=mongodb://localhost:27017/appointment-system
JWT_SECRET=your_jwt_secret_key_here
```

### 启动项目

```bash
# 开发模式 - 同时启动前后端
npm run dev

# 仅启动后端
npm start

# 仅启动前端（在 client 目录下）
cd client
npm run dev
```

### 访问地址
- 前端: http://localhost:5173
- 后端 API: http://localhost:8080

## API 接口

### 用户接口
- `POST /api/user/register` - 用户注册
- `POST /api/user/login` - 用户登录
- `GET /api/user/profile` - 获取用户信息

### 医生接口
- `POST /api/doctor/apply` - 申请成为医生
- `GET /api/doctor/list` - 获取医生列表
- `GET /api/doctor/profile/:id` - 获取医生详情

### 预约接口
- `POST /api/user/book-appointment` - 创建预约
- `GET /api/user/my-appointments` - 获取我的预约

### 管理员接口
- `GET /api/admin/users` - 获取用户列表
- `GET /api/admin/doctors` - 获取医生列表
- `POST /api/admin/doctor/:id/status` - 更新医生状态

## 开发说明

### 代码规范
- 使用 ESLint 进行代码检查
- 遵循 Airbnb JavaScript 风格指南

### 提交规范
- `feat`: 新增功能
- `fix`: 修复 bug
- `docs`: 文档更新
- `style`: 代码格式调整
- `refactor`: 代码重构

## 许可证

MIT License
