# 페미위키

한국의 페미니즘 위키 [페미위키]에 대한 기술 정보 개괄 및 기타 이슈 트래킹용 Repository.

## 개요

페미위키는 [Terraform]에 의해 [AWS] 상에서 복수의 서버로 운영되고 있으며 각 서버는 [Docker]를 통해 여러 서비스를 실행하고 있습니다. 일부 Docker image는 페미위키에서 제작한 것으로 [Docker Hub]를 통해 배포되고 있습니다.
또 페미위키는 '페미위키 스킨'을 비롯한 몇 개의 미디어위키 플러그인을 개발하여 사용하고 있습니다.

## Repositories

- [서버](https://github.com/femiwiki?q=docker-compose+server)
- [Docker Image](https://github.com/femiwiki?q=docker-image)
- [Amazon Machine Image](https://github.com/femiwiki/ami)
- 미디어위키 플러그인
  - [페미위키 스킨](https://github.com/femiwiki/FemiwikiSkin)
  - [확장 기능](https://github.com/femiwiki?q=mediawiki-extension)

## 현황

아래는 페미위키가 사용중인 웹 서비스 등의 현황입니다.

### 서버

[Amazon EC2](https://aws.amazon.com/ec2/)를 사용하며 다음과 같이 가상 서버를 운영중입니다.

이름 | 기능 | 서버 수
-----|------|-----
[mediawiki] | mediawiki를 비롯한 웹 서버 | 1
[database] | MySQL과 웹 서버의 캐시, 크론잡 등 | 1

### 기타

아래 서비스를 사용중입니다. [Terraform]을 통해 관리되고 있어 [femiwiki/infra] Repository를 참고할 수 있습니다.

- [Amazon Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)
- [Amazon S3](https://aws.amazon.com/s3/)
- [Amazon Simple Email Service](https://aws.amazon.com/ses/)
- [Amazon Route53](https://aws.amazon.com/route53/)

## 이슈 트래킹

이슈는 종류에 따라 각각의 Repository에 위치하며, 전반적인 서버 관리 등 해당하는 Repository가 없는 경우에는 이 Repository(femiwiki/femiwiki)에 작성됩니다. 페미위키는 또한 이슈를 포함한 계획과 목표를 관리하기 위해 [Github의 프로젝트 보드](https://github.com/orgs/femiwiki/projects/1)를 사용하고 있습니다.

이슈나 버그에 있을 때는 언제든 편히 남겨주세요.

## 라이센스

페미위키의 코드는 기본적으로 AGPLv3 라이선스로 공개되어 있으며, 자세한 정보는 각 Repository 별로 명시되어 있습니다.
(AGPLv3는 미디어위키의 라이선스 정책인 "GPLv2 혹은 그 이상"과 호환됩니다. 자세한 정보는 [GNU FAQ](https://www.gnu.org/licenses/gpl-faq.en.html#v2v3Compatibility)를 참고하세요)

&nbsp;

--------

The source code of *femiwiki/femiwiki* is primarily distributed under the terms
of the [GNU Affero General Public License v3.0] or any later version. See
[COPYRIGHT] for details.

[페미위키]: https://femiwiki.com
[aws]: https://aws.amazon.com
[terraform]: https://terraform.io
[docker]: https://docker.com/
[docker hub]: https://hub.docker.com/u/femiwiki/
[mediawiki]: https://github.com/femiwiki/mediawiki
[database]: https://github.com/femiwiki/database
[femiwiki/infra]: https://github.com/femiwiki/infra
[gnu affero general public license v3.0]: LICENSE
[copyright]: COPYRIGHT
