# Ozon Watch Product Catalog

公开的单 SKU 手表资料货盘。每个商品目录对应一个确定款式，同型号不同颜色分别保留，不合并。

## 目录

```text
products/<brand>/<sku>/
  1.jpg ... N.jpg
  product_facts.json
  ozon_listing_template.json
  上架资料.md
  catalog_status.json
```

- 根目录 `catalog.json` 只索引通过本地图片、单 SKU 和 Ozon 手表类目必填字段校验的商品。
- `1.*` 是主图，后续图片按数字顺序使用；图片数量以当前 SKU 原图为准。
- `catalog_ready` 是待激活货盘状态，不代表已经创建 Ozon 商品。
- 公开文件不保存采购商业值、最终售价、目标店铺或任何凭据。
- 上架会话激活单品后会在私有环境生成独立的 `ready_to_list` 包；本仓库不执行店铺写入或库存操作。

## 数据边界

商品事实来自当前 SKU 的 `描述.txt` 与同目录原图。平台可选属性只在有文字证据时填写；无法从资料确认的可选属性保留缺失状态，不从 AI 图片或相似商品推测。

