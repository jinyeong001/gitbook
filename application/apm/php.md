---
description: 해당 포스트의 과정은 RedHat 계열의 리눅스 서버(Rocky Linux)에서 진행되었습니다.
---

# 2. PHP

## # PHP 란?

PHP(Hypertext Preprocessor)는 서버 사이드 스크립팅 언어로, HTML에 임베드되어 동적 웹 페이지를 생성할 수 있다.\
HTML과 달리 서버에서 실행되어 데이터베이스 연동, 파일 처리 등 다양한 서버 측 기능을 제공한다.



### 1. PHP 설치 및 테스트

```bash
# PHP 설치
$ dnf install -y php php-mysqlnd

# Apache 재시작
$ systemctl restart httpd
```



### 2. PHP  테스트 페이지

```php
# /var/www/html/info.php
<?php
    phpinfo();
?>
```



### 3. HTML vs PHP 예제

```php
# /var/www/html/example.php
<!DOCTYPE html>
<html>
<body>
    <!-- HTML 부분 -->
    <h1>정적 콘텐츠</h1>
    
    <!-- PHP 부분 -->
    <?php
        $time = date("Y-m-d H:i:s");
        echo "<p>현재 시간: $time</p>";
        
        // 간단한 계산
        $a = 5;
        $b = 3;
        echo "<p>$a + $b = " . ($a + $b) . "</p>";
    ?>
</body>
</html>
```



## # 작동 확인

브라우저 주소창에서 `http://서버IP/info.php` 접속
