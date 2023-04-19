# Introduction

- `Golang`, `Go`는 `Google`이 2009년 11월에 개발했습니다.
- 간단한 구문, 동시성 용이, 컴파일 언어, 정적 링크, 자동 가비지콜렉션 등이 장점

## Installation

https://golang.org/dl/

- How to Check if you installed Go?

```bash
go version
```

! 2023-04-19 기준, `go1.20.3`

## go.mod

-> 생성했더니, gopls를 설치하라는 추천 문구가 vscode에서 등장했다.

- [`gopls`](ang.org/x/tools/gopls): 쉽게 말해, 자동 완성 지원!

- `go.mod`는 코드에 대한 종속성 추적을 활성화한다.
  - 종속성 패키지 라이브러리: https://pkg.go.dev/
  - import `something` 형식으로 코드에 종속성 추가 가능
- 의존성이 추가되면, `go.sum`파일이 생성되어 의존 모듈의 체크섬을 저장
  - go module에 대한 mirror, index, checksum Database: https://proxy.golang.org/
- 기본 라이브러리 (Standard Library): https://pkg.go.dev/std

## HOW TO RUN

```bash
go run .
```

- RESULT \*

```bash
Hello, World!
Don't communicate by sharing memory, share memory by communicating.
```

## Standard Package 말고 External Package를 추가해볼까?

- 종속성 패키지 라이브러리에서 패키지를 찾은 후, 상단 BreadCrumb 에 `rsc.io/quote/v4`와 같이 복사할 수 있는 버튼이 있다. 얘를 복사해서 import 구문에 추가하자!
- 그리고 go mod tidy를 하면, 다운로드하지 않은 모듈을 찾아서 다운로드한다.
