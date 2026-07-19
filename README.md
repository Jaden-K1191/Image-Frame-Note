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
- 미등록 제조사는 EXIF 제조사명을 텍스트 브랜드로 표시
- 이미지 로고 지원 템플릿에서 사용자 제조사 로고 추가(PNG, SVG, WebP, JPEG · 최대 2MB)
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
- Brush Photo Edge

### Brush Photo Edge

`Brush Photo Edge`는 사진의 네 면을 붓으로 칠한 듯 불규칙하게 표현하는 프레임입니다. 스타일 탭의 전용 드롭다운에서 A–F 6가지 엣지를 선택할 수 있습니다. 프레임 색상은 사진 바깥쪽 캔버스 색으로 사용되며, 저작자와 워터마크 표시를 지원합니다.

## 브랜드 로고

앱에는 주요 브랜드 로고가 포함되어 있습니다.

- Fujifilm
- Leica
- Canon
- Nikon
- Sony
- Sony Alt Logo
- Lumix
- Lumix Alt Logo
- OM System
- Ricoh

Sony Alt Logo와 Lumix Alt Logo는 어두운 배경에서 사용할 수 있는 흰색 로고입니다.

스타일 탭에서 `EXIF 제조사명 (텍스트)`을 선택하면 목록에 없는 카메라 제조사도 EXIF의 `Make` 값을 그대로 브랜드명으로 표시할 수 있습니다. `EXIF에서 자동`을 선택한 경우에도 등록되지 않은 제조사는 Fujifilm로 대체하지 않고 EXIF 제조사명이 텍스트로 출력됩니다.

Journal B, Contact Sheet C, Gallery Frame, Poster Overlay, Minimal Bottom Bar처럼 이미지 로고를 표시하는 템플릿에서는 `사용자 제조사 로고 추가` 버튼으로 로고를 불러올 수 있습니다. PNG, SVG, WebP, JPEG를 지원하며 투명 PNG 또는 자체 포함형 SVG를 권장합니다. Film Date Overlay처럼 제조사명을 문자로 표시하는 템플릿과 로고가 없는 템플릿에서는 이 버튼이 표시되지 않습니다.

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


## Final Patch — 저작자 및 워터마크

- 저작자 표시 요소 추가: © 저작자, Photo by 저작자, Copyright © 연도 저작자, 이름만 표시
- 텍스트 또는 이미지 워터마크 지원
- 워터마크 이미지 색상 변경 및 크기·X·Y 위치 조정
- 저작자 표시의 색상·크기·X·Y 위치 조정
- Thought / Note의 수동 줄바꿈 시 불필요한 빈 줄이 생기거나 두 번째 줄이 잘리는 문제 수정


## iPhone / iPad
- HEIC/HEIF 사진을 불러오면 브라우저 안에서 JPEG 미리보기로 변환하고, 원본 HEIC의 EXIF를 읽습니다.
- 지원되는 iPhone/iPad에서는 `원본 · 사진 앱으로` 또는 `웹용 · 사진 앱으로` 버튼이 나타납니다.
- 버튼을 누른 뒤 iOS 공유 시트에서 `이미지 저장`을 선택하면 사진 앱에 저장됩니다. 웹 브라우저 보안상 앱이 사용자 확인 없이 사진 보관함에 직접 저장할 수는 없습니다.

## Film Date Overlay segment display
Film Date Overlay uses an embedded 16-segment vector display renderer. It does not depend on an external font file, so the preview and exported JPEG remain consistent across iPhone/iPad, Windows, macOS, Chrome, Edge and Safari.



## Brush Photo Edge — 샘플 누끼 마스크 방식

- 대화에서 확정한 6종 샘플 이미지의 외곽 실루엣을 직접 분리해 A~F 알파 마스크로 적용했습니다.
- 브라우저 계산으로 임의 프레임을 만드는 방식이 아니라, 각 샘플의 실제 네 면 형태를 고정 마스크로 사용합니다.
- 흰색 하늘·건물처럼 사진 내부의 밝은 영역은 투명해지지 않도록 외곽 연결 영역 기준으로 분리했습니다.
- 마스크는 `app.js`에 내장되어 로컬 실행과 iPhone 환경에서 별도 경로 로딩 없이 동작합니다.
- 원본 PNG 마스크와 확인용 미리보기는 `assets/brush_masks/`에도 포함했습니다.


## Brush Photo Edge 자산형 렌더링 추가

이번 버전부터 Brush Photo Edge 템플릿은 **마스크(mask) + 텍스처 오버레이(overlay)** PNG 자산을 읽을 수 있습니다.

- 경로: `assets/brush_photo_edge/`
- 파일명 예시: `A_landscape_mask.png`, `A_landscape_overlay.png`
- 비율 그룹: `landscape`, `portrait`, `square`
- 자산이 없을 경우 기존 내장 Brush Photo Edge 로직으로 자동 fallback 됩니다.

자세한 제작 규칙은 `assets/brush_photo_edge/README.md`를 확인하세요.


## 포함된 A 스타일 기본 자산

이 패키지에는 `Brush Photo Edge A`용 자산이 기본 포함되어 있습니다.

포함 파일:
- `A_landscape_mask.png`
- `A_landscape_overlay.png`
- `A_portrait_mask.png`
- `A_portrait_overlay.png`
- `A_square_mask.png`
- `A_square_overlay.png`

`assets/brush_photo_edge/` 폴더의 preview 파일로 대략적인 적용 느낌을 확인할 수 있습니다.

B ~ F 스타일은 현재 기존 fallback 방식으로 동작합니다.


## 포함된 Brush Photo Edge 자산

현재 패키지에는 A~F 전체 스타일용 기본 자산이 포함되어 있습니다.

- A: landscape / portrait / square
- B: landscape / portrait / square
- C: landscape / portrait / square
- D: landscape / portrait / square
- E: landscape / portrait / square
- F: landscape / portrait / square

각 스타일은 `mask + overlay` 구조로 구성되어 있으며, `assets/brush_photo_edge/` 폴더에서 직접 교체하거나 세부 조정할 수 있습니다.


### Brush Photo Edge patch
- A keeps the subtle asset-based look you liked.
- B~F were rebuilt to be visually distinct while staying restrained, instead of all collapsing into the same look.


## Photo Data layout and lens EXIF update
- Portrait photos now use the same layout as landscape photos: photo on the left and data panel on the right.
- Lens display priority: `LensModel`; when unavailable, fall back to `Lens`.
- `LensInfo` and `LensSpecification` are not merged into the displayed lens name.
- ISO remains formatted as `ISO 250`, with one space between ISO and the numeric value.


## New in this update
- Added **Multi Frame** template.
- Supports `Hero + Two · Landscape`, `Hero + Two · Portrait`, `Triple Strip`, and `Diptych`.
- Current selected image is used as the first/main tile, and the remaining images are placed in list order. Photos are never duplicated to fill missing slots; missing slots remain empty placeholders.
- Supports square (1:1), 4:5, and 3:2 output ratios.


## Multi Frame update
- Multi Frame now preserves the original photo aspect ratio.
- Added optimized layouts: Hero + Two · Landscape, Triple Strip · Panorama, Double Stack · Landscape, Diptych · Portrait.
- Multi Frame is intentionally simple: no EXIF, title, location, logo, creator, or watermark overlays.
- Overall frame ratio is derived from the inserted photos and selected layout.

- Added **Hero (Portrait) + Two Mini (Landscape)** with aspect-ratio-preserving geometry.
