[페미위키]
========
페미위키 깃헙에 오신것을 환영합니다!

페미위키는 모든 소스코드를 오픈소스로 공개하고있으며, 이슈트래커와 대화공간도
공개하고있어 페미위키 구성원이 아닌사람도 페미위키 개발에 쉽게 참여하실 수
있습니다.

- [각종 소스코드](https://github.com/femiwiki/)
- [페미위키 디스코드 #개발 채널](https://discord.gg/yrQCFQt)
- [페미위키 이슈 트래커](https://github.com/femiwiki/femiwiki/issues)
- [페미위키 개발팀 칸반 보드](https://github.com/orgs/femiwiki/projects/1)
- [페미위키 개발팀 주별/분기별 목표](https://github.com/femiwiki/femiwiki/milestones)

페미위키에 이슈나 버그, 원하시는 건의사항이 있으실 경우 언제든지 편하게 이슈를
남겨주세요.

&nbsp;

페미위키 기술 개요
--------
페미위키는 [AWS]를 사용하고있으며, [Terraform]을 사용해 선언적으로 클라우드
인프라를 관리하고있습니다. 페미위키에선 [Docker] 컨테이너를 사용해 서비스들을
배포하고있으며, [Docker Hub]에서 누구나 페미위키 컨테이너 이미지를 다운받을 수
있습니다. 페미위키는 미디어위키 엔진을 사용하고있고, [FemiwikiSkin],
[Sanctions] 등 여러 미디어위키 확장을 자체개발하여 사용하고있습니다.

[페미위키]: https://femiwiki.com
[AWS]: https://aws.amazon.com
[Terraform]: https://terraform.io
[Docker]: https://docker.com/
[Docker Hub]: https://hub.docker.com/u/femiwiki/
[FemiwikiSkin]: https://github.com/femiwiki/FemiwikiSkin
[Sanctions]: https://github.com/femiwiki/Sanctions

주로 작업하는 소스코드들은 아래 링크로 확인하실 수 있으십니다.

- [페미위키 테라폼](https://github.com/femiwiki/infra)
- [도커 컴포즈 목록](https://github.com/femiwiki?q=docker-compose+server)
- [도커 이미지 목록](https://github.com/femiwiki?q=docker-image)
- [페미위키 서버 AMI](https://github.com/femiwiki/ami)
- 미디어위키 플러그인
  - [FemiwikiSkin]
  - [그 외 자체 개발 확장 기능들](https://github.com/femiwiki?q=mediawiki-extension)

&nbsp;

이용 허락
--------
페미위키 코드들은 기본적으로 "GNU Affero General Public License version 3"
라이선스로 공개되어 있지만, 간혹 불가피하게 다른 라이센스를 사용하는 경우가
있습니다. 정확한 정보는 각 Repository 안에있는 `LICENSE` 파일을 참고해주세요.

AGPL-3.0은 미디어위키의 라이선스 정책인 "GPL-2.0 혹은 그 이상"과 호환됩니다.
자세한 정보는 [GNU FAQ]를 참고해 주세요.

[GNU FAQ]: https://www.gnu.org/licenses/gpl-faq.en.html#v2v3Compatibility

&nbsp;

--------

The source code of *femiwiki/femiwiki* is primarily distributed under the terms
of the [GNU Affero General Public License v3.0] or any later version. See
[COPYRIGHT] for details.

[GNU Affero General Public License v3.0]: LICENSE
[COPYRIGHT]: COPYRIGHT
