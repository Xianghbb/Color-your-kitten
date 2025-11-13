# 🐱 Color Your Kitten - 小猫遗传模拟器

An interactive web app that simulates how kitten coat colors and patterns are formed through genetic inheritance.

一个互动式的网页应用，通过遗传学原理模拟小猫的毛色和花纹的形成过程，让用户体验猫咪育种的乐趣与挑战。

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

## 📖 项目简介

Color Your Kitten 是一个游戏化的教育应用，将复杂的猫咪遗传学知识转化为有趣的互动体验。用户可以：

- 选择亲代猫咪进行配对
- 观察和学习基因如何影响毛色和花纹
- 生成独一无二的小猫
- 收集稀有毛色和品种
- 理解孟德尔遗传定律在现实中的表现

## ✨ 主要功能

### 🎮 核心游戏功能
- **猫咪配对系统**：选择不同的父母猫进行繁殖
- **基因可视化**：直观展示显性和隐性基因的表达
- **毛色生成器**：基于真实遗传算法生成小猫毛色
- **收藏系统**：收集并展示你培育的所有小猫
- **稀有度系统**：通过概率计算稀有毛色的出现

### 🧬 遗传学特性
- **真实遗传算法**：基于猫科动物真实遗传机制
- **多基因控制**：支持颜色、花纹、眼睛颜色等多特征的基因
- **基因型与表现型**：区分基因组合和实际外观
- **遗传概率计算**：基于孟德尔遗传定律的概率分布

### 🌟 其他功能
- **猫咪图鉴**：完整的猫咪毛色和品种百科全书
- **成就系统**：解锁不同的繁殖挑战和目标
- **分享功能**：分享你培育的独特小猫
- **教育模式**：详细的遗传学知识解释

## 🛠 技术栈

### 前端
- **React 18** - UI 框架
- **React Router** - 路由管理
- **Redux Toolkit** - 状态管理
- **TypeScript** - 类型安全
- **Tailwind CSS** / **Styled Components** - 样式框架
- **Framer Motion** - 动画效果
- **Canvas API** / **SVG** - 猫咪图形渲染

### 后端
- **Node.js 18+** - 运行时环境
- **Express.js** - Web 框架
- **TypeScript** - 类型安全
- **Mongoose** - MongoDB ODM
- **JWT** - 身份认证
- **Bcrypt** - 密码加密
- **Joi** - 数据验证

### 数据库
- **MongoDB** - NoSQL 数据库
  - 用户信息集合
  - 猫咪基因数据集合
  - 育种记录集合
  - 收藏和成就数据集合

### 部署 & 云服务 (AWS)
- **Amazon EC2** - 应用服务器托管
- **Amazon S3** - 猫咪图片和静态资源存储
- **Amazon CloudFront** - CDN 加速
- **Amazon Route 53** - DNS 管理
- **AWS Certificate Manager** - SSL 证书管理
- **Amazon CloudWatch** - 监控和日志
- **AWS Elastic Beanstalk** / **Docker** - 容器化部署

### 开发工具
- **Git** - 版本控制
- **ESLint + Prettier** - 代码规范
- **Husky** - Git 钩子
- **Jest + React Testing Library** - 单元测试
- **Cypress** - E2E 测试
- **Webpack / Vite** - 构建工具

## 📁 项目架构

```
Color-your-kitten/
├── client/                     # React 前端应用
│   ├── public/
│   ├── src/
│   │   ├── components/        # React 组件
│   │   ├── pages/             # 页面组件
│   │   ├── store/             # Redux 状态管理
│   │   ├── services/          # API 服务
│   │   ├── utils/             # 工具函数
│   │   ├── types/             # TypeScript 类型定义
│   │   └── App.tsx           # 根组件
│   └── package.json
│
├── server/                    # Node.js 后端服务
│   ├── src/
│   │   ├── controllers/       # 控制器逻辑
│   │   ├── models/            # Mongoose 模型
│   │   ├── routes/            # API 路由
│   │   ├── middleware/        # 中间件
│   │   ├── services/          # 业务逻辑
│   │   ├── utils/             # 工具函数
│   │   └── app.ts            # Express 应用
│   └── package.json
│
├── shared/                    # 前后端共享代码
│   ├── types/                 # 共享类型定义
│   └── constants/             # 共享常量
│
├── scripts/                   # 构建和部署脚本
└── docker-compose.yml         # Docker 容器配置
```

## 🚀 快速开始

### 前置要求

- Node.js 18.0 或更高版本
- MongoDB 5.0 或更高版本
- npm 或 yarn 包管理器

### 本地安装

1. **克隆仓库**
   ```bash
   git clone https://github.com/your-username/Color-your-kitten.git
   cd Color-your-kitten
   ```

2. **安装后端依赖**
   ```bash
   cd server
   npm install
   ```

3. **安装前端依赖**
   ```bash
   cd ../client
   npm install
   ```

4. **配置环境变量**

   在 `server/` 目录下创建 `.env` 文件：
   ```env
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/kitten-genetics
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

   在 `client/` 目录下创建 `.env` 文件：
   ```env
   REACT_APP_API_URL=http://localhost:5000
   REACT_APP_APP_ENV=development
   ```

5. **启动 MongoDB**
   ```bash
   mongod --dbpath=./data
   ```

6. **运行后端服务器**
   ```bash
   cd server
   npm run dev
   ```

7. **运行前端开发服务器**
   ```bash
   cd client
   npm start
   ```

8. **访问应用**

   打开浏览器访问：`http://localhost:3000`

## 📊 数据结构

### 猫咪基因模型

```typescript
{
  // 基础颜色基因 (B, b)
  blackGene: 'B' | 'b',
  // 橙色基因 (X)
  orangeGene: 'X' | 'x',
  // 稀释基因 (D, d)
  diluteGene: 'D' | 'd',
  // 重点色基因 (C, cs, cb, ca)
  colorpointGene: 'C' | 'cs' | 'cb' | 'ca',
  // 白色斑点基因 (S, s)
  whiteSpottingGene: 'S' | 's',
  // 斑纹基因 (T, ta, tb)
  tabbyGene: 'T' | 'ta' | 'tb',
  // 重点色表达 (取决于 colorpointGene)
  hasColorpoint: boolean
}
```

### 毛色表现型

基于基因组合，系统生成以下特征：

- **基础颜色**: 黑色系 / 橙色系
- **稀释色**: 蓝色、巧克力色、奶油色等
- **重点色**: 暹罗猫型重点色
- **花纹**: 虎斑纹、鲭鱼纹、经典纹
- **白斑**: 从少量到双色分布

## 🔧 遗传算法核心逻辑

本项目基于以下遗传学原理实现：

### 1. 孟德尔遗传定律
- **分离定律**: 每个亲代提供一半的基因
- **自由组合定律**: 不同基因的独立分配

### 2. 显性与隐性
```
黑色基因: B (显性) vs b (隐性)
橙色基因: X链 (性连锁遗传)
稀释基因: D (显性) vs d (隐性, 产生稀释色)
```

### 3. 性连锁遗传
橙色基因只存在于X染色体上：
- 公猫: XY - 一个橙色基因决定颜色
- 母猫: XX - 两个橙色基因产生玳瑁/三花

### 4. 基因互作
- 上位效应: 一个基因抑制另一个基因的表达
- 多基因控制: 多个基因共同影响一个性状

## 🎨 毛色生成算法示例

```typescript
// 计算后代基因
function calculateOffspringGenes(parent1: Cat, parent2: Cat): Gene {
  const offspringGene = {};

  // 对每对基因位点
  for (const geneLocus in parent1.genes) {
    // 每个亲代随机提供一个等位基因
    const allele1 = randomlySelectFrom(parent1.genes[geneLocus]);
    const allele2 = randomlySelectFrom(parent2.genes[geneLocus]);

    // 组合成后代基因型
    offspringGene[geneLocus] = allele1 + allele2;
  }

  return offspringGene;
}

// 基因型转换为表现型
function genotypeToPhenotype(genes: Gene): CatAppearance {
  return {
    baseColor: determineBaseColor(genes),
    pattern: determinePattern(genes),
    isDiluted: checkDilution(genes),
    hasWhite: checkWhiteSpotting(genes),
    eyeColor: determineEyeColor(genes)
  };
}
```

## 🌐 部署指南

### AWS 部署流程

1. **构建前端**
   ```bash
   cd client
   npm run build
   ```

2. **上传静态资源到 S3**
   ```bash
   aws s3 sync build/ s3://your-kitten-app-bucket/ --delete
   ```

3. **配置 CloudFront**
   - 创建 CloudFront 分配
   - 设置源为 S3 bucket
   - 配置 SSL 证书

4. **部署后端**
   ```bash
   cd server
   npm run build
   ```

   使用 Elastic Beanstalk 或 EC2 部署。

5. **配置 Route 53**
   - 设置域名解析
   - 指向 CloudFront 分配

### Docker 部署

```bash
# 构建镜像
docker build -t color-your-kitten .

# 运行容器
docker run -p 80:80 --env-file .env color-your-kitten
```

## 🖼 界面预览

### 主界面
- 展示区：查看你收集的猫咪
- 配对区：选择父母猫
- 结果区：查看新生成的小猫

### 基因实验室
- 可视化基因组合
- 预测后代可能性
- 学习遗传学知识

### 猫咪图鉴
- 完整的毛色收藏
- 品种信息
- 稀有度展示

## 📚 遗传学知识库

### 基础猫毛颜色基因

| 基因类型 | 代表字母 | 功能 |
|---------|---------|------|
| 黑色基因 | B/b | 产生黑色素 |
| 橙色基因 | O | 产生红色素（性连锁）|
| 稀释基因 | D/d | 稀释色素浓度 |
| 白色基因 | W/w | 控制白斑分布 |
| 斑纹基因 | T/ta/tb | 产生虎斑花纹 |
| 重点色基因 | C/cs/cb/ca | 重点色表达 |

### 常见猫咪毛色
- **纯色**: 全黑、全橙、全灰
- **虎斑纹**: 鲭鱼纹、经典纹、斑点纹、 ticked纹
- **重点色**: 暹罗猫型、缅甸猫型
- **三花/玳瑁**: 性连锁遗传的独特表现
- **烟色/银色**: 毛尖着色

## 🤝 贡献指南

欢迎 Contributions！请在开始前：

1. Fork 本仓库
2. 创建新的分支 (`git checkout -b feature/amazing-feature`)
3. 提交你的改动 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建 Pull Request

### 开发规范
- 使用 TypeScript 进行开发
- 遵循 ESLint 和 Prettier 配置
- 编写单元测试和集成测试
- 确保代码覆盖率高于 80%

### 待办事项
- [ ] 更多猫咪品种
- [ ] 长毛/短毛基因
- [ ] 眼睛颜色遗传
- [ ] 多代谱系系统
- [ ] 社区分享功能
- [ ] 遗传学课程模块
- [ ] 3D 猫咪模型
- [ ] 移动 App 版本

## 📄 许可证

本项目采用 MIT 许可证。详见 [LICENSE](LICENSE) 文件。

## 👨‍💻 作者

- Your Name - Initial work - [GitHub](https://github.com/your-username)

## 📧 联系方式

- 项目链接: [https://github.com/your-username/Color-your-kitten](https://github.com/your-username/Color-your-kitten)
- 问题反馈: [Issues](https://github.com/your-username/Color-your-kitten/issues)
- 邮箱: your.email@example.com

## 🙏 致谢

- 感谢所有猫科遗传学研究者
- 启发来自猫咪爱好者社区
- 特殊感谢对本项目贡献的开发者们

---

<div align="center">
  <strong>🐾 Made with ❤️ for cat lovers and genetics enthusiasts 🧬</strong>
</div>
