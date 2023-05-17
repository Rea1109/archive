## SQL 모음집

> 자주 사용하는 SQL 저장소

```sql
    -- 게시물 조회 order by , limit 사용
    SELECT * FROM boards ORDER BY board_id DESC LIMIT 0,5 ;

    -- total count
    SELECT COUNT(*) FROM boards;

    -- column 값(숫자) 자동증가 query
    ALTER TABLE boards AUTO_INCREMENT 100;
```