# ReviewTab

A review workspace for confidential journal peer review, for reviewers who want a language model's
help without sending manuscripts to services that keep them.

**Download:** [Releases](https://github.com/junhewk/reviewtab/releases). This repository holds the
release files, this page and the licence only; the source code is not published.

[한국어](#한국어) · [English](#english)

## 한국어

ReviewTab은 학술지 심사를 위한 검토 작업 공간입니다. 원고를 열고 논증도, 구간 검토, 인용 확인과
검토자 메모로 심사를 정리합니다. 원고를 열고 메모하는 데에는 모델이 필요하지 않으며, 모델 작업은
범위를 보여 준 뒤 승인할 때에만 실행합니다. 화면은 한국어와 영어를 지원합니다.

### 모델과 원고

- 모델은 이 컴퓨터나 개인 네트워크의 모델, 또는 데이터를 보관하지 않는 OpenRouter(ZDR)만 쓸 수
  있습니다. 그 밖의 서비스는 거부합니다.
- 원고는 이 컴퓨터에서 읽고, 승인한 작업에 필요한 부분만 고른 모델로 보냅니다. 참고문헌 조회는
  승인할 때에만 학술 데이터베이스로 보냅니다. 제작자에게는 아무것도 보내지 않습니다.
- 어떤 모델을 쓸지, 학술지의 기밀 유지와 AI 사용 규정을 지키는지는 검토자가 판단합니다.
- 모든 사이트를 읽을 수 있는 브라우저 확장 프로그램은 화면의 원고도 읽을 수 있습니다. 그런
  확장이 없는 브라우저나 프로필을 권합니다.

### 설치와 시작

[Releases](https://github.com/junhewk/reviewtab/releases)에서 운영체제에 맞는 파일을 받아 원하는
폴더에 풉니다. 따로 설치할 프로그램은 없습니다.

| 운영체제 | 파일 | 시작 |
| --- | --- | --- |
| Windows 10/11 (x64) | `reviewtab-VERSION-windows-x64.zip` | `ReviewTab.bat` 두 번 클릭. 'PC 보호' 경고가 보이면 '추가 정보' > '실행' |
| macOS 11 이상 (Apple silicon) | `reviewtab-VERSION-macos-arm64.tar.gz` | `ReviewTab.command` 두 번 클릭. 막히면 시스템 설정 > 개인정보 보호 및 보안 > '그래도 열기' |
| Linux (x64, glibc 2.28 이상) | `reviewtab-VERSION-linux-x64.tar.gz` | 터미널에서 `./reviewtab.sh` |

브라우저에서 ReviewTab이 열립니다. 작업하는 동안 시작 창을 열어 두고, 끝내려면 그 창을 닫습니다.
검토 자료는 앱 폴더와 따로 저장되므로, 새 버전은 새 폴더에 풀어 쓰면 됩니다. 자세한 내용은
압축 안의 `README.txt`에 있습니다.

### 받은 파일 확인

Releases의 `SHA256SUMS`와 받은 파일의 SHA-256 값을 비교합니다.

```
sha256sum -c SHA256SUMS --ignore-missing          # Linux
shasum -a 256 -c SHA256SUMS --ignore-missing      # macOS
certutil -hashfile reviewtab-VERSION-windows-x64.zip SHA256   # Windows
```

### 라이선스

무료로 제공하는 사용 허락이며 수정, 재배포, 역설계는 허용하지 않습니다. [LICENSE.md](LICENSE.md)를
읽어 주세요. 함께 들어 있는 오픈 소스 구성 요소의 라이선스는 압축 안의
`THIRD_PARTY_NOTICES.txt`에 있습니다.

## English

ReviewTab is a review workspace for journal peer review. Open a manuscript and work through it
with an argument diagram, section review, citation checks and your own notes. Opening a
manuscript and taking notes need no model; a model task runs only after it shows its scope and
you approve it. The interface is in Korean and English.

### Models and manuscripts

- Models can only be ones on your computer or a private network, or OpenRouter with zero data
  retention (ZDR). Other services are refused.
- Manuscripts are read on your computer. Only the part an approved task needs is sent to the
  model you chose. Reference lookups go to scholarly databases only when you approve them.
  Nothing is sent to the author.
- Which model to use, and whether a journal's confidentiality and AI-use policies allow it, is
  the reviewer's decision.
- Browser extensions allowed to read all sites can also read the manuscript on the page. A
  browser or profile without them is advised.

### Install and start

Download the file for your system from [Releases](https://github.com/junhewk/reviewtab/releases)
and unpack it into any folder. Nothing else needs to be installed.

| System | File | Start |
| --- | --- | --- |
| Windows 10/11 (x64) | `reviewtab-VERSION-windows-x64.zip` | Double-click `ReviewTab.bat`. If Windows says it protected your PC, choose More info > Run anyway |
| macOS 11 or later (Apple silicon) | `reviewtab-VERSION-macos-arm64.tar.gz` | Double-click `ReviewTab.command`. If blocked, choose Open Anyway in System Settings > Privacy & Security |
| Linux (x64, glibc 2.28 or later) | `reviewtab-VERSION-linux-x64.tar.gz` | Run `./reviewtab.sh` in a terminal |

ReviewTab opens in your browser. Keep the start window open while you work and close it to quit.
Your reviews are kept apart from the app folder, so a new version is simply unpacked into a new
folder. `README.txt` in the archive has the details.

### Check a download

Compare the file's SHA-256 with `SHA256SUMS` from the release:

```
sha256sum -c SHA256SUMS --ignore-missing          # Linux
shasum -a 256 -c SHA256SUMS --ignore-missing      # macOS
certutil -hashfile reviewtab-VERSION-windows-x64.zip SHA256   # Windows
```

### Licence

ReviewTab is free to use under its own licence, which does not allow modification,
redistribution or reverse engineering: read [LICENSE.md](LICENSE.md). The open-source components
it includes, and their licences, are listed in `THIRD_PARTY_NOTICES.txt` in the archive.
