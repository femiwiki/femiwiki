# CHANGELOG

[페미위키]와 관련되어 있지만 소스코드 외의 내용이라 추적이 어려운 변경 사항에 대한 기록으로, 시간 표기는 대략적인 것입니다.

## 2019-10

- **[2019-10-19T05:03+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-18](https://github.com/femiwiki/mediawiki/releases/tag/build-18)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>
- **[2019-10-12T06:09+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/commit/207f3d4)
- **[2019-10-12T05:07+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-17](https://github.com/femiwiki/mediawiki/releases/tag/build-17)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>

## 2019-09

- **[2019-09-21T06:24+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 내 파일 수정
  <details>https://raw.githubusercontent.com/femiwiki/DiscordNotifications/a67b7b7/i18n/ko.json 파일 생성</details>
- **[2019-09-21T06:20+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-15](https://github.com/femiwiki/mediawiki/releases/tag/build-15)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>
- **[2019-09-11T05:00+0900]** database+bots 인스턴스의 MySQL과 Memcached 버전 업.
  <details>https://github.com/femiwiki/femiwiki/issues/89 작업과 함께 MySQL 8.0.13 → 8.0.17, Memcached 1.5.12 → 1.5.17 업그레이드</details>

## 2019-08

- **[2019-08-17T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-14](https://github.com/femiwiki/mediawiki/releases/tag/build-14)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>
- **[2019-08-10T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-13](https://github.com/femiwiki/mediawiki/releases/tag/build-13)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>

## 2019-07

- **[2019-07-20T08:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 내 파일 수정(https://github.com/femiwiki/mediawiki/commit/0e5b979)
- **[2019-07-20T06:10+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 내 파일 수정(https://github.com/femiwiki/skin/commit/3600b47)
- **[2019-07-20T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-12](https://github.com/femiwiki/mediawiki/releases/tag/build-12)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>
- **[2019-07-13T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-11](https://github.com/femiwiki/mediawiki/releases/tag/build-11)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포</details>
- **[2019-07-09T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-10](https://github.com/femiwiki/mediawiki/releases/tag/build-10)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포, 미디어위키 1.32.3 업그레이드 등.</details>

## 2019-06

- **[2019-06-26T01:43+0900]** database+bots 인스턴스의 bots_rankingbot 콘테이너 이미지를 [build-2](https://github.com/femiwiki/rankingbot/releases/tag/build-2)로 교체함.
- **[2019-06-26T01:26+0900]** database+bots 인스턴스의 bots_rankingbot 콘테이너 이미지를 [build-1](https://github.com/femiwiki/rankingbot/releases/tag/build-1)로 교체함.
- **[2019-06-13]** mediawiki 인스턴스 문제 해결(https://github.com/femiwiki/femiwiki/issues/84)

## 2019-05

- **[2019-05-09T15:50+0900]** database+bots 인스턴스에서 사용중인 Volume의 타입을 standard에서 gp2로 변경(https://github.com/femiwiki/femiwiki/issues/81)
- **[2019-05-08T18:34+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 내 파일 수정(https://github.com/femiwiki/skin/commit/b752208)
- **[2019-05-04T05:03+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-9](https://github.com/femiwiki/mediawiki/releases/tag/build-9)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기 배포, 미디어위키 1.32.1 업그레이드 등.</details>
- **[2019-05-01T17:51+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/commit/1b30e97)
  <details>편집 필터 관련 권한 조정</details>

## 2019-04

- **[2019-04-28T13:16+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/commit/31de71b)
  <details>디스코드 알림 설정 변경</details>
- **[2019-04-27T14:57+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/commit/8e042b3)
  <details>Seeder 권한 편집 허용</details>
- **[2019-04-22T16:11+0900]** database+bots 인스턴스에 atop 설치함. 나중에 다시 삭제해야함 자세한것은 [#64](https://github.com/femiwiki/femiwiki/issues/64) 참고.
- - **[2019-04-22T02:30+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/compare/ae7d725...14e91dc)
  - **[2019-04-20T05:08+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-8](https://github.com/femiwiki/mediawiki/releases/tag/build-8)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  - **[2019-04-20T05:00+0900]** mediawiki 인스턴스의 femiwiki 스택과 femiwiki_files 볼륨을 재생성함. (실수로 빌드 버전 안올림)
  - **[2019-04-20T04:59+0900]** mediawiki 인스턴스의 `/home/ec2-user/mediawiki/configs/secret.php` 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/a4d262e).

  <details>정기배포. DiscordNotifications 확장기능 설치.</details>

- **[2019-04-18T15:06+0900]** mediawiki 인스턴스 `/home/ec2-user/configs/mediawiki/`의 LocalSettings.php 및 secret.php 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/c3ab22d)
  <details>구글 통계 ID 이동</details>
- **[2019-04-18T14:14+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 파일 수정(https://github.com/femiwiki/mediawiki/commit/a55eafc)
  <details>차단 보조기능 활성화</details>
- **[2019-04-17T22:15+0900]** mediawiki 인스턴스의 femiwiki_files 볼륨 내 파일 직접 수정(https://github.com/femiwiki/skin/commit/5a5531c)
  <details>가입 질문 복사 방지</details>
- - **[2019-04-16T16:50+0900]** database+bots 인스턴스의 bots_backupbot 콘테이너 이미지를 [build-5](https://github.com/femiwiki/backupbot/releases/tag/build-5)로 교체함
  - **[2019-04-17T16:24+0900]** S3 버킷 라이프사이클 "Transition mysql dumps to Glacier Deep Archive after 14 days" 생성
  - **[2019-04-16T14:08+0900]** database+bots 인스턴스의 bots_backupbot 콘테이너 이미지를 [build-4](https://github.com/femiwiki/backupbot/releases/tag/build-4)로 교체함
  - **[2019-04-15T16:05+0900]** S3 버킷 라이프사이클 삭제함

  <details>

  https://github.com/femiwiki/femiwiki/issues/73 백업 비용 최적화함. 기존에는 S3에 백업하고 2주 뒤에 Glacier로 옮겼는데, 이제 기본으로 S3 IA에 백업하고 2주 뒤에 Glacier Deep Archive로 옮기도록 수정함.

  S3의 femiwiki-backups 버킷에 저장되는 데이터가 데이터베이스 백업뿐 아니라 그 외 여러가지가 되어, 데이터베이스 백업은 `/mysql/`에 저장하고 그 외 파일은 잠정적으로 루트 경로에 보관하기로 함.

  </details>

- **[2019-04-13T06:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-7](https://github.com/femiwiki/mediawiki/releases/tag/build-7)로 교체하면서 femiwiki_files 볼륨도 재생성함.

  <details>정기 배포. UnifiedExtensionForFemiwiki 확장기능 업데이트.</details>

- **[2019-04-11T17:30+0900]** mediawiki 인스턴스에서 사용되지 않는 도커 이미지 삭제함.
  <details>일부 문서가 표시되지 않고 자바스크립트가 작동하지 않아 원인 파악 중 [하드디스크 문제](https://github.com/femiwiki/femiwiki/issues/70#issuecomment-482030123)로 밝혀져 조치함.</details>

## 2019-03

- **[2019-03-31T22:00+0900]** mediawiki 인스턴스의 `/home/ec2-user/configs/mediawiki/LocalSettings.php` 및 `/home/ec2-user/mediawiki/configs/secret.php` 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/b533083)
  <details>스팸 계정이 급증함에 따라 구글 reCAPTCHA를 발급받아 사용하기로 함.</details>
- **[2019-03-29T16:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-6](https://github.com/femiwiki/mediawiki/releases/tag/build-6)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>PHP 7.2.15 → PHP 7.2.16 업그레이드 등</details>
- **[2019-03-23T04:30+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-5](https://github.com/femiwiki/mediawiki/releases/tag/build-5)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기배포.</details>
- **[2019-03-20T16:00+0900]** mediawiki 인스턴스의 `/home/ec2-user/mediawiki/configs/LocalSettings.php` 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/f25fb5b)
- **[2019-03-19T23:14+0900]** mediawiki 인스턴스의 femiwiki_files 볼륨 내 파일 직접 수정(https://github.com/femiwiki/skin/commit/a13c3f7)
  <details>이메일 발신 장애 리포트에 따라 조치함.</details>
- **[2019-03-16T06:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-4](https://github.com/femiwiki/mediawiki/releases/tag/build-4)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기배포.</details>
- **[2019-03-16]** database+bots 인스턴스의 bots_backupbot 콘테이너 이미지를 [build-2](https://github.com/femiwiki/backupbot/releases/tag/build-2)로 교체함
  <details>백업 횟수를 줄여 짝수일에만 실행되도록 함, 이에 따라 2019-03-17T05:00+0900 백업 이후 2019-03-18T05:00+0900 백업은 생략되고 2019-03-19T05:00+0900에 진행됨, 이후 동일.</details>
- **[2019-03-10T18:06+0900]** database+bots 인스턴스의 bots_backupbot 콘테이너 이미지를 [build-1](https://github.com/femiwiki/backupbot/releases/tag/build-1)로 교체함.
- **[2019-03-10T15:30+0900]** database+bots 인스턴스의 bots_backupbot 콘테이너 안에서 `nice -n 19 mysqldump --compress --single-transaction femiwiki | nice -n 19 gzip -9 | /usr/local/bin/aws s3 cp - s3://femiwiki-backups/test/`를 실행하여 성공함.
  <details>데이터베이스 백업을 위해 우선 파일을 생성하고 그 파일을 업로드하던 것을 파일을 생성하지 않도록 수정함.</details>
- **[2019-03-09T23:20+0900]** mediawiki 인스턴스의 `/home/ec2-user/mediawiki/configs/LocalSettings.php` 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/a265c4e)
- **[2019-03-09T06:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-3](https://github.com/femiwiki/mediawiki/releases/tag/build-3)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기배포. 미디어위키 1.32.0 업그레이드 등.</details>

## 2019-02

- **[2019-02-23T05:00+0900]** mediawiki 인스턴스의 femiwiki_mediawiki 콘테이너 이미지를 [build-1](https://github.com/femiwiki/mediawiki/releases/tag/build-1)로 교체하면서 femiwiki_files 볼륨도 재생성함.
  <details>정기배포.</details>
- - **[2019-02-15T06:00+0900]** mediawiki 인스턴스에서 사용되지 않는 도커 이미지 삭제하여 mediawiki 스택 정상 실행됨.
  - **[2019-02-15T05:00+0900]**

    - mediawiki 인스턴스의 `/home/ec2-user/mediawiki/configs/LocalSettings.php` 파일 직접 수정(https://github.com/femiwiki/mediawiki/commit/0fdbb34)
    - database+bots 인스턴스에서 femiwiki/restbase:build-0 도커 컨테이너 삭제.
    - mediawiki 인스턴스에서 mediawiki 스택 재생성(femiwiki/restbase:build-1 도커 컨테이너 추가됨). 하드디스크 용량 문제로 정상 실행에 실패함.
    - database+bots 인스턴스에서 femiwiki/cassandra:build-0 도커 컨테이너 실행.

  <details>정기배포 및 RESTBase가 실행되는 장소(서버)를 옮기고 데이터베이스를 SQLite(기본값)에서 카산드라로 교체함.</details>

[페미위키]: https://femiwiki.com
