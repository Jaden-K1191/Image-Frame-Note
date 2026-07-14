# FrameNote Web App

FrameNote는 사진에 프레임, 텍스트, EXIF, 브랜드 로고를 적용하고 JPEG로 저장하는 브라우저 기반 앱입니다.
사진과 입력 내용은 브라우저 안에서 처리됩니다.

## 실행

압축을 푼 뒤 폴더에서 로컬 웹 서버를 실행하는 방식을 권장합니다.

```bash
cd FrameNote_WebApp_Final
python -m http.server 8000
```

브라우저에서 아래 주소를 엽니다.

```text
http://localhost:8000
```

Chrome 또는 Edge 사용을 권장합니다.

## 주요 기능

- JPEG, PNG, WebP 사진 불러오기
- 여러 장 사진 동시 업로드
- 사진별 제목, 본문, 위치, 프로젝트, 별점, 질문 문구 입력
- JPEG EXIF 자동 읽기 및 직접 수정
- 카메라 브랜드 자동 판별 및 로고 표시
- 템플릿별 표시 요소 선택
- 제목, 본문, 위치, 로고, EXIF 등의 위치·크기·행간 조절
- 일괄 적용 모드와 사진별 개별 작업 모드
- 현재 사진 원본/웹용 JPEG 저장
- 전체 사진 원본/웹용 일괄 저장
- 지원 브라우저에서 사용자가 선택한 폴더에 직접 저장
- 폴더 저장 미지원 시 ZIP 또는 일반 다운로드 사용
- OTF, TTF, WOFF, WOFF2 사용자 폰트 추가

## 여러 장 작업

1. `사진 추가`에서 여러 장을 선택합니다.
2. 좌측 사진 목록에서 작업할 사진을 선택합니다.
3. `일괄 적용 모드`를 켜면 템플릿과 스타일 변경이 전체 사진에 적용됩니다.
4. `일괄 적용 모드`를 끄면 사진마다 템플릿과 스타일을 따로 설정할 수 있습니다.
5. 좌측의 `원본 전체 다운로드` 또는 `웹용 전체 다운로드`로 결과물을 한 번에 저장합니다.

일괄 저장은 사진을 한 장씩 순차 처리해 브라우저 메모리 사용량을 줄입니다. 원본 출력이 브라우저의 안전 픽셀 한도를 넘으면 자동으로 안전한 크기로 축소될 수 있습니다.

## 저장 폴더 선택

Chrome 또는 Edge에서는 `저장 폴더 선택` 버튼으로 출력 위치를 직접 지정할 수 있습니다.

- 현재 사진 저장: 선택한 폴더에 JPEG 직접 저장
- 전체 저장: 결과물을 한 장씩 선택한 폴더에 직접 저장
- 동일한 파일명이 존재하면 번호를 붙여 별도 저장

브라우저가 폴더 직접 저장을 지원하지 않으면 기존 다운로드 또는 ZIP 저장 방식이 사용됩니다.

## 템플릿

- Journal B
- Contact Sheet C
- Gallery Frame
- Film Date Overlay
- Poster Overlay
- Clean Frame
- Minimal Bottom Bar
- Exhibition Caption
- Polaroid Note

## 브랜드 로고

앱에는 주요 브랜드 로고가 포함되어 있습니다.

- Fujifilm
- Leica
- Canon
- Nikon
- Sony
- Sony Alt Logo
- OM System
- Ricoh

Sony Alt Logo는 어두운 배경에서 사용할 수 있는 밝은 로고입니다.

## 폰트

기본 웹폰트는 네트워크 연결이 필요한 경우가 있습니다. 사용자 폰트는 스타일 탭의 `추가 폰트 관리`에서 불러올 수 있습니다.

지원 형식:

- OTF
- TTF
- WOFF
- WOFF2

사용자가 추가한 폰트는 브라우저 저장소에 보관되며, 선택한 폰트만 메모리에 불러옵니다.

## 주의사항

- 브라우저 저장소를 삭제하면 사용자 설정과 추가한 폰트가 초기화될 수 있습니다.
- Safari에서는 저장 폴더 선택이나 대용량 Canvas 처리가 제한될 수 있습니다.
- JPEG 내보내기 전에 선택한 사용자 폰트와 로고가 미리보기에 정상 표시되는지 확인하십시오.


## 저작권 및 이용 안내

- Copyright © 2026 Jaden_fujipuerson (KIM JEONGHA). All rights reserved.
- FrameNote로 제작한 결과 이미지는 개인 및 상업적 사진 작업에 사용할 수 있습니다.
- FrameNote 프로그램 자체의 판매, 무단 재배포, 재패키징 및 수정본 공개 배포는 허용되지 않습니다.
- 브랜드 로고, 폰트 및 외부 라이브러리의 권리는 각 권리자에게 있습니다.
- 자세한 조건은 `LICENSE.txt`와 `THIRD_PARTY_NOTICES.txt`를 확인하세요.


## 저작권 및 이용 안내

앱 상단의 `i` 버튼에서 저작권 및 이용 안내를 확인할 수 있습니다. 안내는 한국어를 먼저 표시하고 영어를 함께 제공합니다. 상세 내용은 `LICENSE.txt`와 `THIRD_PARTY_NOTICES.txt`에 한국어 우선 순서로 수록되어 있습니다.

## 문의 / Contact

저작권, 배포 허가 및 권리 관련 문의:

- restinmylife@naver.com

이 연락처는 저작권 및 배포 관련 문의를 위한 것이며, 개별 사용법 안내나 기술 지원을 보장하지 않습니다.

Copyright, distribution-permission, and rights inquiries:

- restinmylife@naver.com

This contact is provided for copyright and distribution-related inquiries. Individual usage assistance or technical support is not guaranteed.
