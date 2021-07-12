# Go Tour (Go를 향한 여행)
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

이 repository는 https://tour.golang.org 의 한국어 번역을 위한 repository 입니다.



## 배포하는 방법

> 현재는 배포가 GCP의 `go-lang-ko` 프로젝트의 권한이 있는 사람에 의해 수동으로 진행되고 있습니다.
> 누군가 Github Action을 통해 자동화를 진행해주시기를 기다리고있습니다.

<!-- `app.yaml`속의 `service`를 수정해주십시오. --> 

```bash
$ GO111MODULE=on gcloud --project=go-tour-ko app deploy app.yaml
$ gcloud app browse
```



## Contribute하기

golang-ko의 tour는 누구든 자유롭게 기여하실 수 있고, 이를 매우 환영합니다!

간단한 오타 수정이나 추가 번역의 경우 바로 PR을 남겨주셔도 되고, 간단히 Issue를 남겨주시면
누군가 빠른 시일 내에 참고하여 처리할 것입니다.

이슈를 남기고, 본인이 직접 해결해보고자하시는 분은 이슈에 해당 내용을 언급해주시면 감사하겠습니다.

많은 Contribute를 기대합니다! 감사합니다!

### Contribute 전에 로컬에서 확인해보는 방법

```bash
# git clone 후 project root에서 실행
$ go run .
2020/09/02 16:59:17 Serving content from <YOUR_LOCATION>/tour
2020/09/02 16:59:17 A browser window should open. If not, please visit http://127.0.0.1:3999
```

### 번역파일 작성 시 주의사항

* 띄어쓰기를 주의해주세요.
  * ⭕ \`hello\` World => `hello` World
  * ❌ \`hello\`World => \`hello\`World
  
  * ⭕ \*하나\*더\*주의:\* => **하나 더 주의:**
  * ❌ \*하나 더 주의:\* => \*하나 더 주의:\*
  
* `#appengine`은 appengin으로 실행한 경우에만 보여지고, 그렇지 않은 경우는 생략된 채 다음 줄의 문장으로 치환됩니다.
  * ```
    #appengine: foo
    bar
    ```
  * appengine으로 서브: foo
  * 그 외의 경우로 서브: bar

---

# _ORIGINAL(English) README.md_

# Go Tour

A Tour of Go is an introduction to the Go programming language. Visit
https://tour.golang.org to start the tour.

## Download/Install

To install the tour from source, first
[install Go](https://golang.org/doc/install) and then run:

	$ go get golang.org/x/tour

This will place a `tour` binary in your
[workspace](https://golang.org/doc/code.html#Workspaces)'s `bin` directory.
The tour program can be run offline.

## Contributing

Contributions should follow the same procedure as for the Go project:
https://golang.org/doc/contribute.html

To run the tour server locally:

```sh
go run .
```

Your browser should now open. If not, please visit [http://localhost:3999/](http://localhost:3999).


## Report Issues / Send Patches

This repository uses Gerrit for code changes. To learn how to submit changes to
this repository, see https://golang.org/doc/contribute.html.

The issue tracker for the tour's code is located at https://github.com/golang/go/issues.
Prefix your issue with "x/tour:" in the subject line, so it is easy to find.

Issues with the tour's content itself should be reported in the issue tracker 
at https://github.com/golang/tour/issues.

## Deploying

1.	To deploy tour.golang.org, run:

	```
	GO111MODULE=on gcloud --project=golang-org app deploy --no-promote app.yaml
	```

	This will create a new version, which can be viewed within the
	[golang-org GCP project](https://console.cloud.google.com/appengine/versions?project=golang-org&serviceId=tour).

2.	Check that the deployed version looks OK (click the version link in GCP).

3.	If all is well, click "Migrate Traffic" to move 100% of the tour.golang.org
	traffic to the new version.

4.	You're done.

## License

Unless otherwise noted, the go-tour source files are distributed
under the BSD-style license found in the LICENSE file.

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://umi0410.github.io"><img src="https://avatars.githubusercontent.com/u/33250725?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jinsu Park</b></sub></a><br /><a href="#infra-umi0410" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a> <a href="https://github.com/golang-ko/tour/pulls?q=is%3Apr+reviewed-by%3Aumi0410" title="Reviewed Pull Requests">👀</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!