# 打卡应用 (Check-In App)

Next.js + Prisma (MongoDB) 实战教学项目

## 课前准备

### 1. 配置数据库连接

1. 注册 [MongoDB Atlas](https://www.mongodb.com/atlas) 免费账号
2. 创建免费集群，获取连接串
3. "cp env.example .env", 编辑 `.env` 文件，替换连接串DATABASE_URL

### 2. 安装依赖

```bash
npm install
```

### 3. 生成 Prisma 客户端

```bash
npx prisma generate
```

## 常用命令

| 命令 | 说明 |
|------|------|
| `npx prisma studio` | 打开可视化数据库管理界面 |
| `npx prisma db push` | 将 Schema 同步到数据库 |
| `npx prisma generate` | 生成 Prisma 客户端 |

## 课程学习路径

1. **选型分析**：使用「5问选型法」确定数据库类型
2. **模型设计**：用自然语言描述需求，AI 生成 Prisma Schema
3. **数据同步**：执行 push，将模型同步到 MongoDB Atlas
4. **增删改查**：通过 Prisma Studio 或 API 操作数据
5. **报错排查**：掌握常见错误的解决方法

## 数据模型设计

参考 Schema 文件 `prisma/schema.prisma`，包含：

- **CheckIn（打卡记录）**：支持灵活字段（健身/读书/工作等）
- 不需要预先定义所有字段，体现非关系型的灵活性
- 支持嵌套数据、数组类型
