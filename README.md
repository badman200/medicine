# 药品目录查询系统

一个现代化的医保药品目录查询系统，使用React + TypeScript + Tailwind CSS构建。

## 功能特性

- 🏥 **四个药品分类**：西药部分、中成药部分、协议西药、协议中成药
- 🔍 **智能搜索**：支持药品名称关键词搜索
- 📂 **分类筛选**：左侧分类树，支持主分类和子分类筛选
- 📄 **分页显示**：右侧药品列表，支持分页浏览
- 🎨 **现代化UI**：使用Tailwind CSS和Radix UI组件库
- 📱 **响应式设计**：支持桌面和移动设备

## 技术栈

- **前端框架**：React 19 + TypeScript
- **样式框架**：Tailwind CSS
- **UI组件**：Radix UI + 自定义组件
- **图标**：Lucide React
- **构建工具**：Vite

## 快速开始

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

### 构建生产版本

```bash
npm run build
```

## 项目结构

```
src/
├── components/
│   └── ui/           # UI组件库
│       ├── button.tsx
│       ├── card.tsx
│       ├── input.tsx
│       ├── pagination.tsx
│       ├── select.tsx
│       └── tabs.tsx
├── lib/
│   └── utils.ts      # 工具函数
├── App.tsx           # 主应用组件
└── main.tsx          # 应用入口
```

## 数据格式

系统使用JSON格式的药品数据，包含以下结构：

```json
{
  "西药部分": {
    "categories": {
      "XA": {
        "code": "XA",
        "name": "消化道和代谢方面的药物",
        "subcategories": {
          "XA02A": {
            "code": "XA02A",
            "name": "抗酸药"
          }
        }
      }
    },
    "medicines": [
      {
        "id": "unique_id",
        "name": "药品名称",
        "category_code": "XA",
        "category_name": "分类名称",
        "subcategory_code": "XA02A",
        "subcategory_name": "子分类名称",
        "dosage": "剂型",
        "note": "备注",
        "payment_standard": ["支付标准"],
        "validity_period": "有效期"
      }
    ]
  }
}
```

## 开发说明

- 使用TypeScript确保类型安全
- 采用组件化设计，便于维护和扩展
- 支持深色模式（通过CSS变量实现）
- 使用Framer Motion实现流畅的动画效果

## 许可证

MIT License
