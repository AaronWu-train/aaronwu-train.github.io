---
# 頁面標題
title: "Posts"

# 使用 Landing Page 模板，才能解析 sections 底下的 block
type: landing

design:
  # Section spacing
  spacing: "5rem"

# 分頁設定（每頁顯示 9 篇，可依需求調整）
params:
  pagination:
    enable: true
    perPage: 9

# 這段用來傳遞給主樣版，關閉 max-width 並顯示麵包屑
cascade:
  - _target:
      kind: page
    params:
      show_breadcrumb: true
      container: full

# 區塊式頁面：用 collection block 列出 posts 資料夾底下文章
sections:
  - block: collection
    id: posts
    content:
      title: "Posts"
      count: 0
      filters:
        folders:
          - posts
      # 依日期排序（遞減）
      sortBy: date
      order: descending
    design:
      view: article-grid # 卡片式格子顯示
      columns: 1 # n欄排版
      fill_image: true # 卡片圖像不強制填滿
      gap: 1.5rem # 卡片之間的間距
      max_width: none # 取消內建的寬度限制
---
