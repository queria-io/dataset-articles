# Queria ショーケース

[Queria のショーケース](https://queria.io/showcase)に載っているレポートのタイトル・概要・公開日・使っているデータセット・タグを収録したデータセットです。

## テーブル

`main.mart_articles` は 1 行が 1 レポートです。

| 列 | 内容 |
| --- | --- |
| `slug` | レポートの一意な識別子 |
| `title` | タイトル |
| `description` | 概要 |
| `date` | 公開日 |
| `datasources` | 使っているデータセット |
| `tags` | タグ |
| `search_text` | タイトル・概要・タグを結合した検索用の文字列 |

## 使い方

「人口」を含むレポートを新しい順に並べる:

```sql
SELECT slug, title, date
FROM articles.main.mart_articles
WHERE search_text LIKE '%人口%'
ORDER BY date DESC;
```
