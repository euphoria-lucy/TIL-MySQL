# 🍀 MySQL 설치하기

## 🧸 MySQL 설치

1. MySQL Community 다운로드 링크 클릭
2. MySQL Server, MySQL Workbench 다운로드 및 설치
3. Sakila database 다운로드

### ⛄ 윈도우의 경우 MySQL Installer for Windows로 한 번에 설치

- MySQL Community Server
- MySQL Workbench
- Sample Database

<br>

## 🧸 MySQL Workbench 사용하기

- **localhost** 로 연결 생성
- 설정했던 비밀번호로 **root** 계정 접속
- 데이터베이스 생성

  ```mysql
  CREATE SCHEMA `mydatabase` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci ;
  ```

  - mydatabase 라는 스키마 생성
  - 기본 캐릭터셋으로 UTF-8, MB4
  - 정렬방식 COLLATE

<br>

| 항목                     | 사용 이유                                      |
| ------------------------ | ---------------------------------------------- |
| `utf8mb4`                | 한글을 포함한 전세계 문자 + 이모티콘 사용 가능 |
| `utf8mb4 _ general _ ci` | 가장 정확하지는 않지만 정렬 속도 빠름          |

```mysql
-- 데이터베이스 삭제 명령어
DROP DATABASE `mydatabase`;
```

<br>

## 🧸 Sakila Database 설치

- Sakila Database 다운로드

1. File > Open SQL Script > ...sakila-schema.sql
2. File > Open SQL Script > ...sakila-data.sql

br>

## 🧸 CLI로 실행해보기

터미널 또는 파워쉘에서 MySQL이 설치된 폴더로 이동

- 윈도우 **C:\Program Files\MySQL\MySQL Server 8.0\bin**
- 맥 : **/usr/local/mysql/bin**

```
./mysql -u root -p
```

```
use sakila;
```
