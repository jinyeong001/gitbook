---
description: 해당 포스트의 과정은 RedHat 계열의 리눅스 서버(Rocky Linux)에서 진행되었습니다.
---

# 3. MySQL (MariaDB)

## # MariaDB 란?

MariaDB는 MySQL의 대체 데이터베이스로, MySQL과 완벽한 호환성을 제공하는 오픈소스 관계형 데이터베이스이다.



### 1. MariaDB 설치 및 초기 설정

```bash
# MariaDB 설치
$ dnf install -y mariadb-server

# 서비스 시작 및 자동 시작 설정
$ systemctl start mariadb
$ systemctl enable mariadb

# 초기 보안 설정
$ mysql_secure_installation
```

#### 기본 보안 설정 과정

1. root 비밀번호 설정
2. 익명 사용자 제거
3. 원격 root 로그인 비활성화
4. test 데이터베이스 제거
5. 권한 테이블 재로드



### 2. 데이터베이스 접속

```bash
$ mysql -u root -p
```



### 3. 기본 데이터베이스 명령어

```sql
# 데이터베이스 생성
$ CREATE DATABASE mydb;

# 사용자 생성 및 권한 부여
$ CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'password';
$ GRANT ALL PRIVILEGES ON mydb.* TO 'myuser'@'localhost';
$ FLUSH PRIVILEGES;
```



## # 추가 데이터베이스 명령어

자세한 데이터베이스 명령어는 [SQL문법](../../database/mysql/sql-language.md) 페이지를 참고하세요.
