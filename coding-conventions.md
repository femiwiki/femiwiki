# Coding Conventions

## PHP

- [미디어위키의 Coding Conventions]을 따르며 [mediawiki/mediawiki-codesniffer]
  검사에 오류가 없으면 문제가 없는 것으로 합니다.

## JavaScript / TypeScript / JSON / CSS

- [Biome]의 기본값(탭, 큰따옴표, 후행 쉼표 `all`)을 따릅니다. `biome ci`가
  포맷, 권장 린트 규칙, import 정렬을 검사합니다.
- 저장소마다 검사에서 뺄 파일(translatewiki가 관리하는 `i18n/`, 생성된 파일
  등)은 그 저장소의 `.biome.json`에 적습니다.

## LESS

- Biome이 LESS를 지원하지 않아 [Prettier]를 탭 들여쓰기로 적용합니다.

## Markdown

- [rumdl]을 적용합니다. 단, release-please가 생성하는 `CHANGELOG.md`는 예외로
  둡니다.
- 봇이 쓰는 Markdown은 커밋하기 전에 `rumdl fmt`를 거칩니다.

## YAML

- [yamllint]를 `--strict`로 적용합니다.

## Python

- [Ruff]의 `ruff check`와 `ruff format --check`를 적용합니다. 줄 길이와 추가
  규칙은 저장소마다 `pyproject.toml`에 적습니다.

## Shell Script

- [ShellCheck]를 적용합니다. 포맷 도구는 두지 않습니다.

## TOML

- [Taplo]의 `taplo fmt --check`를 적용합니다.

## Dockerfile

- [Hadolint]를 적용합니다.

## GitHub Actions

- 워크플로는 [actionlint]와 [zizmor]로 검사합니다.

## Lua

- [StyLua]를 적용합니다.

## Terraform

- [terraform fmt] 적용
- `.tf`를 스크립트로 고칠 때는 `sed`나 문자열 치환 대신 [hcledit]으로 속성이나
  블록을 주소로 지정해 고칩니다. 주변 코드가 스크립트의 예상과 달라도 엉뚱한 곳을
  고치지 않습니다.

  ```sh
  hcledit attribute set locals.schema_update_generation 145 -f locals.tf -u
  hcledit attribute get resource.docker_container.http.image -f container.tf
  ```

## HCL

- [hclfmt] 적용

## Golang

- [golangci-lint]를 적용하며, 포맷은 golangci-lint의 gofmt와 goimports
  포매터로 검사합니다.

## Mustache

- 미정. 아직 검사 도구가 없습니다.

## Actions 시크릿

- 한 워크스페이스만 쓰는 femiwiki/infra 시크릿은
  `<워크스페이스>_<이름>`(`AWS_LOKI_PASSWORD`, `GRAFANA_MASTODON_TOKEN`), tofu
  워크플로 전체가 쓰는 것은 `TOFU_<이름>`으로 짓습니다. `GITHUB_`로 시작하는
  이름은 GitHub가 받지 않습니다.
- PR plan도 읽는 시크릿은 저장소 시크릿에, plan이 읽지 않는
  시크릿(`GRAFANA_APPLY_TOKEN`)만 환경 시크릿에 둡니다.
- 새 시크릿은 설정 페이지가 아니라 1Password `infra` 보관함 항목과
  femiwiki/infra `github/secrets.tf` 항목으로 추가합니다.

## 커밋 메시지

- CI를 고치는 변경은 버그 수정이라도 `fix(ci):`가 아니라 `ci:`로 적습니다.
  release-please와 [페미위키:업데이트] 노트는 `feat`, `fix`, `perf`를 독자에게
  보이는 변경으로 다루므로, `fix(ci):`는 릴리스와 노트 항목을 불필요하게
  만듭니다.

## 기타

- Biome, Prettier, rumdl, yamllint, zizmor는 femiwiki/.github의
  `shared-lint.yml`이 각 저장소에서 실행합니다. 따로 설치하는 `package.json`은
  두지 않습니다.
- YAML 파일은 `.github/` 아래와 `action.yml`에서 `*.yml`을, 그 밖에서는
  `*.yaml`을 씁니다. 각 저장소 lint의 `extensions` 잡이 검사합니다.

[미디어위키의 coding conventions]: https://www.mediawiki.org/wiki/Special:MyLanguage/Manual:Coding_conventions
[biome]: https://biomejs.dev/
[prettier]: https://prettier.io/
[rumdl]: https://github.com/rvben/rumdl
[yamllint]: https://yamllint.readthedocs.io/
[ruff]: https://docs.astral.sh/ruff/
[shellcheck]: https://www.shellcheck.net/
[taplo]: https://taplo.tamasfe.dev/
[hadolint]: https://github.com/hadolint/hadolint
[actionlint]: https://github.com/rhysd/actionlint
[zizmor]: https://docs.zizmor.sh/
[stylua]: https://github.com/JohnnyMorganz/StyLua
[golangci-lint]: https://golangci-lint.run/
[mediawiki/mediawiki-codesniffer]: https://packagist.org/packages/mediawiki/mediawiki-codesniffer
[terraform fmt]: https://www.terraform.io/docs/cli/commands/fmt.html
[hclfmt]: https://pkg.go.dev/github.com/hashicorp/hcl/v2/cmd/hclfmt
[hcledit]: https://github.com/minamijoyo/hcledit
[페미위키:업데이트]: https://femiwiki.com/w/페미위키:업데이트
