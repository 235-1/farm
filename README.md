# Farm-flo 项目（修改版）

---

## 🚜 项目简介

Farm-flo 是一个农产品电商管理平台，本项目为原作者 [satyam0827](https://github.com/satyam0827/Farm-floooo.git) 的修改版。  
主要优化了购物车功能、前端显示逻辑和后端接口。

**主要功能**：

- 商品浏览与添加购物车
- 修改购物车数量、删除单个商品、清空购物车
- 结算跳转至账单页面
- 前端显示优化，解决删除商品后显示异常问题


## ⚡ 功能优化说明

- **购物车功能**：
  - 删除单个商品后不会影响其他商品显示
  - 修改数量后实时更新合计
  - 清空购物车时返回空列表
- **前端优化**：
  - 增加空购物车提示
  - 修复商品已下架显示异常
- **后端优化**：
  - 删除商品接口返回最新购物车数据
  - 添加商品接口增加数量和价格校验

---

## 🛠 安装和运行

### 克隆项目

```bash
git clone https://github.com/你的用户名/你的仓库名.git
cd 你的仓库名
安装依赖

前端：
cd frontend
npm install

后端：
cd backend
npm install

启动项目

前端（Vite 项目）：
npm run dev

后端：
npm run dev


📦 项目结构
├─ frontend/            # 前端代码
│  ├─ src/
│  │  ├─ components/   # React 组件
│  │  ├─ pages/        # 页面
│  │  └─ store/        # Zustand 状态管理
├─ backend/             # 后端代码
│  ├─ models/           # 数据模型
│  ├─ controllers/      # 控制器
│  └─ routes/           # 路由
├─ package.json
└─ README.md

🔗 API 说明（部分）

获取购物车
GET /api/cart
Headers: Authorization: Bearer <token>

添加商品
POST /api/cart/add
Body: { productId, quantity, price, image }
Headers: Authorization: Bearer <token>

删除商品
DELETE /api/cart/remove
Body: { productId }
Headers: Authorization: Bearer <token>

清空购物车
DELETE /api/cart/clear
Headers: Authorization: Bearer <token>

⚖️ 许可协议
本项目基于原作者项目修改，保留原作者版权信息。
遵守原作者 License（如 MIT），修改部分亦适用相同许可。

📬 联系方式
如有问题，请通过 GitHub Issues 联系我，或者邮箱：x05714ngu@gmail.com