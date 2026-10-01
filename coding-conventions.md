# Coding Conventions

## PHP

- [미디어위키의 Coding Conventions]을 따르며 [mediawiki/mediawiki-codesniffer] 검사에 오류가 없으면 문제가 없는 것으로 합니다.

## JavaScript / JSON

- [Prettier]를 적용합니다.

## CSS / LESS / SCSS

- [Prettier]를 적용합니다.

## XML

- [Prettier]를 적용합니다.

## Markdown

- 미정

## Python

- 미정

## Terraform

- [terraform fmt] 적용

## HCL

- [hclfmt] 적용

## Rust

- 미정

## Golang

- 미정

## Mustache

- 미정

## Ruby

- 미정

## 커밋 메시지

- CI를 고치는 변경은 버그 수정이라도 `fix(ci):`가 아니라 `ci:`로 적습니다. release-please와 [페미위키:업데이트] 노트는 `feat`, `fix`, `perf`를 독자에게 보이는 변경으로 다루므로, `fix(ci):`는 릴리스와 노트 항목을 불필요하게 만듭니다.

## 기타

- YAML 파일은 `.github/` 아래와 `action.yml`에서 `*.yml`을, 그 밖에서는 `*.yaml`을 씁니다. 각 저장소 lint의 `extensions` 잡이 검사합니다.

[미디어위키의 coding conventions]: https://www.mediawiki.org/wiki/Special:MyLanguage/Manual:Coding_conventions
[prettier]: https://prettier.io/
[mediawiki/mediawiki-codesniffer]: https://packagist.org/packages/mediawiki/mediawiki-codesniffer
[terraform fmt]: https://www.terraform.io/docs/cli/commands/fmt.html
[hclfmt]: https://pkg.go.dev/github.com/hashicorp/hcl/v2/cmd/hclfmt
[페미위키:업데이트]: https://femiwiki.com/w/페미위키:업데이트
