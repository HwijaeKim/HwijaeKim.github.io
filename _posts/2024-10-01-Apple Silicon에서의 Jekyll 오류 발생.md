---
title:  "Apple Silicon에서의 Jekyll 오류 발생"
header:
  teaser: "/assets/images/profile.jpg"
categories: 
  - Jekyll
tags:
  - Error
  - Jekyll
  - Mac(Apple Silicon)
---

**1. Xcode Command Line Tools 재설치**
이미 명령줄 도구를 설치했더라도 일부 구성 요소가 손상되었을 수 있으니, 다시 설치하거나 업데이트를 시도해 보세요. 
```
sudo rm -rf /Library/Developer/CommandLineTools
xcode-select --install
```

**2. g++와 clang 설치 확인 및 설정**
macOS에서는 기본적으로 clang을 C++ 컴파일러로 사용합니다. 그러나 환경에 따라 g++ 컴파일러를 사용하는 것이 필요할 수도 있습니다.

• 먼저, clang이나 g++이 설치되어 있는지 확인하세요
```
clang --version
g++ --version
```

• clang이 기본 컴파일러로 설정되어 있는지 확인하기 위해 다음 명령어를 입력해 보세요:
```
brew install gcc
```


```bash
eval $(/opt/homebrew/bin/brew shellenv)
```

