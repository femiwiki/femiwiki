# [페미위키](https://femiwiki.com)

페미위키 깃헙에 오신 것을 환영합니다! 페미위키는 주류 위키들의 남성 중심적이고 여성 혐오적인 정보에 반대하여 약자, 소수자를 위해 만들어진 여성주의 정보 집합체입니다.

페미위키는 모든 소스코드를 오픈소스로 공개하고 있으며, 이슈트래커와 대화공간도
공개하고 있어 페미위키 구성원이 아닌 사람도 페미위키 개발에 쉽게 참여하실 수
있습니다.

- [각종 소스코드](https://github.com/femiwiki/)
- [페미위키 디스코드 #개발 채널](https://discord.gg/umzYjJcbvH)
- [페미위키 이슈 트래커](https://github.com/femiwiki/femiwiki/issues)
- [페미위키 개발팀 칸반 보드](https://github.com/orgs/femiwiki/projects/1)
- [페미위키 개발팀 블로그](https://femiwiki.com/w/Project:%EA%B0%9C%EB%B0%9C_%EB%B8%94%EB%A1%9C%EA%B7%B8)

페미위키에 이슈나 버그, 원하시는 건의사항이 있으실 경우 언제든지 편하게 이슈를
남겨주세요.

## 페미위키 기술 개요

페미위키는 [AWS]를 사용하고 있으며, [Terraform]을 사용해 선언적으로 클라우드
인프라를 관리하고 있습니다. 페미위키에선 [EC2]에 [Nomad]로 [Docker] 컨테이너를 사용해 서비스들을
배포하고 있으며, [Github Container registry]에서 누구나 페미위키 컨테이너 이미지를 다운받을 수
있습니다. 사이트의 일부 정적 리소스는 [S3]에 저장됩니다. AWS SES, Lambda, SQS 등도 사용합니다.

[aws]: https://aws.amazon.com
[terraform]: https://terraform.io
[ec2]: https://aws.amazon.com/ec2
[nomad]: https://www.nomadproject.io/
[docker]: https://docker.com/
[github container registry]: https://github.com/orgs/femiwiki/packages?ecosystem=container
[s3]: https://aws.amazon.com/s3
[ses]: https://aws.amazon.com/ses
[lambda]: https://aws.amazon.com/lambda
[sqs]: https://aws.amazon.com/sqs

페미위키는 [미디어위키] 엔진을 사용하고 있고 [Caddy]를 웹서버로 사용합니다.
데이터베이스는 [MySQL], [Memcached]를 사용합니다.

[미디어위키]: https://www.mediawiki.org
[Caddy]: https://caddyserver.com
[MySQL]: https://www.mysql.com
[Memcached]: https://memcached.org/

미디어위키는 [PHP]와 [Vue.js], [Less.js], [Lua] 등으로 이루어져 있으며 페미위키는 [FemiwikiSkin],
[Sanctions] 등 여러 미디어위키 확장기능을 자체개발하여 사용하고 있습니다.

[php]: https://www.php.net/
[vue.js]: https://vuejs.org/
[less.js]: https://lesscss.org/
[lua]: https://www.lua.org/
[femiwikiskin]: https://github.com/femiwiki/FemiwikiSkin
[sanctions]: https://github.com/femiwiki/Sanctions

페미위키에서 주로 작업하는 소스코드들은 GitHub과 Wikimedia Gerrit에 존재하며 아래 링크로 확인하실 수 있으십니다.

- [페미위키 테라폼](https://github.com/femiwiki/infra)
- [페미위키 Nomad](https://github.com/femiwiki/nomad)
- [도커 이미지 목록](https://github.com/femiwiki?q=docker-image+archived%3Ano)
- 미디어위키 확장기능
  - [FemiwikiSkin]
  - [그 외 자체 개발 확장 기능들](https://github.com/femiwiki?q=mediawiki-extension+fork%3Ano)

## 이용 허락

페미위키 코드들은 기본적으로 "GNU Affero General Public License version 3"
라이선스로 공개되어 있지만, 간혹 불가피하게 다른 라이센스를 사용하는 경우가
있습니다. 정확한 정보는 각 Repository 안에있는 `LICENSE` 파일을 참고해주세요.

AGPL-3.0은 미디어위키의 라이선스 정책인 "GPL-2.0 혹은 그 이상"과 호환됩니다.
자세한 정보는 [GNU FAQ]를 참고해 주세요.

[gnu faq]: https://www.gnu.org/licenses/gpl-faq.en.html#v2v3Compatibility

---

The source code of _femiwiki/femiwiki_ is primarily distributed under the terms
of the [GNU Affero General Public License v3.0] or any later version. See
[COPYRIGHT] for details.

[gnu affero general public license v3.0]: LICENSE
[copyright]: COPYRIGHT
