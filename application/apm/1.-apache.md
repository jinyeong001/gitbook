---
description: 해당 포스트의 과정은 RedHat 계열의 리눅스 서버(Rocky Linux)에서 진행되었습니다.
---

# 1. Apache

## # Apache 란?

Apache HTTP Server는 오픈 소스 웹 서버 소프트웨어로, 전 세계 웹 서버의 큰 비중을 차지하고 있다.\
안정성과 다양한 기능을 제공하며, 모듈 기반 구조로 확장성이 뛰어나다.



### 1. Apache 설치 및 설정

```bash
# Apache 설치
$ dnf install -y httpd

# 서비스 시작 및 자동 시작 설정
$ systemctl start httpd
$ systemctl enable httpd

# 방화벽 설정
$ firewall-cmd --permanent --add-service=http
$ firewall-cmd --reload

# 서비스 상태 확인
$ systemctl status httpd
```



### 2. 웹페이지 생성

기본 문서 경로: `/var/www/html/`

```html
# /var/www/html/index.html 생성
<html>
<body>
    <h1>Welcome to my web server!</h1>
</body>
</html>
```



## # 작동 확인

브라우저 주소창에서 `http://서버IP` 접속

<figure><img src="../../.gitbook/assets/Pasted image 20240826151021.png" alt=""><figcaption><p>Apach default page</p></figcaption></figure>
