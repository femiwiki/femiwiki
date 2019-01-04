# 페미위키

한국의 페미니즘 위키 [페미위키]에 대한 기술 정보 개괄 및 기타 이슈 트래킹용 Repository.

## 개요

페미위키는 [AWS]를 통해 복수의 서버로 운영되고 있으며 각 서버는 [Docker]를 통해 여러 서비스를 실행하고 있습니다. 일부 Docker image는 페미위키에서 제작한 것으로 [Docker Hub]를 통해 배포되고 있습니다.
한편 미디어위키는 플러그인을 지원하며 플러그인들은 확장 기능(Extension) 또는 스킨(Skin)이라는 용어로 지칭되는데, 페미위키에서는 '페미위키 스킨'을 비롯한 몇 개의 플러그인들을 개발하여 사용하고 있습니다.

## Repositories

- [서버](https://github.com/femiwiki?q=docker-compose+server)
- [페미위키에서 제작한 Docker Image](https://github.com/femiwiki?q=docker-image)
- [Amazon Machine Image](https://github.com/femiwiki/ami)
- 페미위키에서 개발한 미디어위키 플러그인
  - [페미위키 스킨](https://github.com/femiwiki/skin)
  - [확장 기능](https://github.com/femiwiki?q=mediawiki-extension)

## 현황

### 서버

[Amazon EC2](https://aws.amazon.com/ec2/)를 사용하여 다음과 같이 가상 서버를 운영중입니다.

|이름|기능|서버 수|
-|-|-
|[mediawiki](https://github.com/femiwiki/mediawiki)|mediawiki를 비롯한 웹 서버|1*|
|[database](https://github.com/femiwiki/database)|MySQL과 웹 서버의 캐시, 크론잡 등|1|

(*) 오토스케일링을 목표로 하고 있어 추후 증가할 수 있음

### 기타

아래 서비스를 사용중입니다.

- [Amazon Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)
- [Amazon S3](https://aws.amazon.com/s3/)
- [Amazon Simple Email Service](https://aws.amazon.com/ses/)
- [Amazon Route53](https://aws.amazon.com/route53/)

## 이슈 트래킹

이슈는 종류에 따라 각각의 Repository에 위치하며, 전반적인 서버 관리 등 해당하는 Repository가 없는 경우에는 이 Repository(femiwiki/femiwiki)에 작성됩니다. 페미위키는 또한 이슈를 포함한 계획과 목표를 관리하기 위해 [Github의 프로젝트 보드](https://github.com/orgs/femiwiki/projects/1)를 사용할 예정입니다.

이슈나 버그에 있을 때는 언제든 편히 남겨주세요.

&nbsp;

--------

The source code of *femiwiki/femiwiki* is primarily distributed under the terms
of the [GNU Affero General Public License v3.0] or any later version. See
[COPYRIGHT] for details.

[페미위키]: https://femiwiki.com
[AWS]: https://aws.amazon.com
[Docker]: https://docker.com/
[Docker Hub]: https://hub.docker.com/
[GNU Affero General Public License v3.0]: LICENSE
[COPYRIGHT]: COPYRIGHT
