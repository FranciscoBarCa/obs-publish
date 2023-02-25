- {{query (and [page-property semester 2] [page-property year 1] )}}
  query-properties:: [:page]

```dataview
  table
  where (degree = "MII" | "MIC") and year = 1 and semester = 2
  ```
  