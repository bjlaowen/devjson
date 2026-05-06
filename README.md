# DevJSON

DevJSON 是一款面向程序员的 JSON 模型转换插件，支持 JSON 格式化、JSON Path 提取、JSON Diff，以及 JSON 与 Go Struct、Proto、TypeScript Interface、Java Class、C# Model、Python Dataclass 的快速转换。以 Chrome 扩展形式运行，点击图标在新标签页打开，数据完全本地处理。

## 功能

**基础工具**

| 标签页 | 说明 |
|---|---|
| 格式化 | JSON 格式化 / 压缩，显示类型与字节大小 |
| 路径提取 | 树形展示 JSON，点击任意字段生成访问路径 |
| JSON Diff | 对比两段 JSON，输出新增 / 删除 / 变化字段 |

**模型转换（JSON → 目标语言）**

| 标签页 | 说明 |
|---|---|
| Go Struct | 生成带 `json` tag 的 Go 结构体 |
| Proto | 生成 proto3 message，支持自定义 package |
| TypeScript | 生成 TypeScript Interface，嵌套类型自动拆分 |
| Java | 生成带 `@JsonProperty` 注解和 getter/setter 的 Java 类 |
| C# | 生成带 `[JsonPropertyName]` 的 C# 属性类 |
| Python | 生成 `@dataclass` 类，子类自动前置 |

**反转工具（目标语言 → JSON）**

| 标签页 | 说明 |
|---|---|
| Go转JSON | 解析 Go Struct，生成字段默认值 JSON 示例 |
| Proto转JSON | 解析 proto message，生成字段默认值 JSON 示例 |

侧边栏支持自定义结构体 / Message 名称、Proto package，并保留最近 20 条本地历史记录。

## 技术栈

- Vue 3 + Vite
- Chrome Extension Manifest V3

## 开发

```bash
npm install
npm run build
```

构建产物在 `dist/` 目录。

## 加载扩展

1. 打开 Chrome，进入 `chrome://extensions/`
2. 开启右上角「开发者模式」
3. 点击「加载已解压的扩展程序」，选择 `dist/` 目录
4. 点击工具栏图标，将在新标签页打开
