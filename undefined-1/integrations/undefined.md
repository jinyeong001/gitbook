# 칼리 리눅스 세팅하기

## # Kali Linux 설치 방법

### 1. 시스템 요구사항

* 최소 2GB RAM (권장 4GB 이상)
* 20GB 하드디스크 공간
* USB 부팅 지원
* 64비트 프로세서

### 2. 설치 과정

1. [공식 웹사이트](https://www.kali.org/)에서 ISO 파일 다운로드
2. 시스템 요구사항에 따른 VM 설정
3. VM 실행 후 기본 설정 후 설치 진행



## # 기본 설정 및 최적화

### 1. 시스템 업데이트

```bash
# 시스템 전체 업데이트
$ sudo apt update
$ sudo apt upgrade -y

# Kali 도구 업데이트
$ sudo apt dist-upgrade -y
```

### 2. Kali 도구 설치

```bash
# 전체 Kali 도구 설치
$ sudo apt install kali-linux-large

# 특정 도구 설치
$ sudo apt install [도구이름]
```



## ⚠️ 주의 사항

{% hint style="danger" %}
### 1. 보안 주의 사항

* 기본 패스워드 변경 필수
* 불필요한 서비스 비활성화
* 방화벽 설정 확인
* 정기적인 업데이트 수행

### 2. 법적 주의 사항

* 허가된 시스템에서만 테스트 수행
* 테스트 범위와 시간 준수
* 결과의 기밀성 유지
* 관련 법규 준수
{% endhint %}

## Reference

{% embed url="https://www.kali.org/docs/" %}

{% embed url="https://forums.kali.org/" %}

{% embed url="https://www.offsec.com/" %}
