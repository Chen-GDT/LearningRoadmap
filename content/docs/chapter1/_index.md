---
# 标题、摘要和页面位置。
linktitle: (翻译测试)第一章
summary: 了解如何使用 Wowchemy 的文档布局档设置，来发布在线课程、软件文档和教程。
weight: 1
icon: book
icon_pack: fas

# Page metadata.
title: 第一章
date: '2024-01-18T00:00:00Z'
type: book # Do not modify.
---

## 灵活性

记录一切！

此灵活性特色功能指可发布如以下内容：

- **在线课程**
- **项目或软件文档**
- **教程**
- **笔记**

原名命为 `courses` 文件夹可以重命名。 例如，我们可以将其重命名为`docs`（用于软件/项目文档）或 `tutorials`（用于创建在线课程）。

## 删除课程

**要删除这些页面，请删除 `courses` 文件夹，然后参见下文删除关联的菜单链接。**

## 更新站点菜单

在完成重命名或删除 `courses` 文件夹后，您可望通过编辑菜单配置文件`config/_default/menus.toml`来更新指向该文件夹中任何“[[main]]”主菜单链接。

例如，如果删除此文件夹，则可以从菜单配置中删除以下内容（toml格式）：

```toml
[[main]]
  name = "课程"
  url = "courses/"
  weight = 50
```

或者，如果您要创建**项目或软件文档**站点，则可以将`courses` 文件夹重命名为“docs”，并将关联的_Courses_菜单配置更新为（toml格式）：

```toml
[[main]]
  name = "營銷项目文档"
  url = "docs/"
  weight = 50
```

## 更新文档菜单

如果您使用 _docs_ 布局，请注意前面的菜单名称应采用 `[menu.X]` 形式，其中 `X` 是文件夹名称。 因此，如果您重命名 `courses/example/` 文件夹，您还应该将`courses/example/` 文件夹中文件的头条材料　(front matter)　的菜单定义值从 `[menu.example]`  改为“[menu.<新文件夹名>” ]`。
