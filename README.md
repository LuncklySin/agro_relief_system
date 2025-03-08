# Agro Relief System - 扶贫惠农推介系统 -- 更多在微信：jackSinWu  -在咸鱼：不知名选手java小鑫

## 项目介绍
扶贫惠农推介系统是一个基于 **个人毕业设计** 的项目，旨在搭建一个在线农业产品推广与销售平台，帮助贫困地区农户拓宽销售渠道，提高农产品的市场竞争力。
![image](https://github.com/user-attachments/assets/ac4ccf8a-396f-4e57-a85d-3b795365e0ec)

## 技术栈
- **前端**：Vue.js + Vuex
- **后端**：Spring Boot + MyBatis + Shiro + Netty
- **数据库**：MySQL
- **存储**：MinIO（对象存储服务）

## 核心功能
### 1. 农产品管理
- 农产品信息发布（名称、图片、价格、产地等）
- 产品分类管理
- 产品库存管理

### 2. 订单管理
- 订单创建、支付与管理
- 订单状态跟踪
- 物流信息管理

### 3. 用户管理
- 账号注册、登录、权限管理（Shiro）
- 农户实名认证
- 个人信息管理

### 4. 推广与推荐
- 农产品推荐算法
- 热销产品展示
- 用户个性化推荐

### 5. 在线客服（Netty 实现）
- 用户与农户在线沟通
- 消息记录存储

### 6. 存储管理（MinIO）
- 农产品图片、用户头像等文件上传与管理

## 项目部署
### 1. 环境要求
- **JDK 11+**
- **Node.js 16+**
- **MySQL 8+**
- **MinIO 服务器**

### 2. 后端启动
```bash
# 进入后端项目目录
cd backend

# 编译打包
mvn clean package

# 运行 Spring Boot
java -jar target/agro-relief-system.jar
```

### 3. 前端启动
```bash
# 进入前端项目目录
cd frontend

# 安装依赖
npm install

# 启动前端项目
npm run serve
```

### 4. MinIO 配置
- 启动 MinIO 服务器：
```bash
minio server /data --console-address ":9001"
```
- 访问 MinIO 控制台：[http://localhost:9001](http://localhost:9001)
- 配置 **Access Key** 和 **Secret Key**，并在后端 `application.yml` 配置 MinIO 连接信息。

## 目录结构
```bash
agro-relief-system/
├── backend/        # 后端 Spring Boot
│   ├── src/main/   # Java 代码
│   ├── resources/  # 配置文件
│   ├── pom.xml     # Maven 配置
│   └── ...
├── frontend/       # 前端 Vue 项目
│   ├── src/        # Vue 代码
│   ├── public/     # 静态资源
│   ├── package.json# 依赖管理
│   └── ...
├── docs/           # 项目文档
├── README.md       # 项目说明
└── ...
```

## 贡献指南
如果你想参与贡献代码，请遵循以下步骤：

1. **Fork 本仓库**
2. **创建新分支** (`git checkout -b feature-xxx`)
3. **提交代码** (`git commit -m '添加新功能 xxx'`)
4. **推送分支** (`git push origin feature-xxx`)
5. **提交 Pull Request**

## 许可证
本项目基于 **MIT License** 进行开源。

---


