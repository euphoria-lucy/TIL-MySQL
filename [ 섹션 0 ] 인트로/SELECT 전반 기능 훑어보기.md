# 🍀 SELECT 전반 기능 훑어보기

## 🧸 SELECT 기능

<br>

### ⛄ 테이블의 모든 내용 보기

```sql
SELECT * FROM Customers;
-- 이와 같이 주석을 달 수 있습니다.
```

- `*` (asterisk) : 테이블의 모든 컬럼을 의미

<br>

### ⛄ 원하는 column(열)만 골라서 보기

```sql
SELECT CustomerName FROM Customers;
```

```sql
SELECT CustomerName, ContactName, Country
FROM Customers;
```

- 💡테이블의 컬럼이 아닌 값도 선택할 수 있음

```sql
SELECT
  CustomerName, 1, 'Hello', NULL
FROM Customers;
```

<br>

### ⛄ 원하는 row(행)만 골라서 보기

- 💡 **WHERE** 구문 뒤에 조건을 붙여 원하는 데이터만 가져올 수 있음

```sql
SELECT * FROM Orders
WHERE EmployeeID = 3;
```

```sql
SELECT * FROM OrderDetails
WHERE Quantity < 5;
```

<br>

### ⛄ 원하는 순서로 데이터 가져오기

- 💡 **ORDER BY** 구문을 사용해서 특정 컬럼을 기준으로 데이터 정렬 가능

| 구문 | 기준     | 기본 |
| ---- | -------- | ---- |
| ASC  | 오름차순 | ✔️   |
| DESC | 내림차순 |      |

```sql
SELECT * FROM Customers
ORDER BY ContactName;
```

```sql
SELECT * FROM OrderDetails
ORDER BY ProductID ASC, Quantity DESC;
```

<br>

### ⛄ 원하는 만큼만 데이터 가져오기

- `LIMIT {가져올 갯수}` 또는 `LIMIT {건너뛸 갯수}, {가져올 갯수}` 를 사용하여, 원하는 위치에서 원하는 만큼만 데이터를 가져올 수 있음

```sql
SELECT * FROM Customers
LIMIT 10;
```

```sql
SELECT * FROM Customers
LIMIT 0, 10;
```

```sql
SELECT * FROM Customers
LIMIT 30, 10;
```

<br>

### ⛄ 원하는 별명 (alias) 으로 가져오기

- 💡 **AS** 를 사용해서 컬럼명을 변경할 수 있음

```sql
SELECT
  CustomerId AS ID,
  CustomerName AS NAME,
  Address AS ADDR
FROM Customers;
```

```sql
SELECT
  CustomerId AS '아이디',
  CustomerName AS '고객명',
  Address AS '주소'
FROM Customers;
```
