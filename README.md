# MOBICAT_concert 저장소 틀 (I-319)

`EarlGreyPie/MOBICAT_concert` 공개 저장소에 그대로 복사해 쓰는 틀입니다. 관객 MOBICAT(0.9.3 이상)은 이 저장소의 **Release 첨부**만 읽습니다.

## 처음 한 번

1. GitHub 에 공개 저장소 `MOBICAT_concert` 를 만들고 이 폴더의 파일을 모두 올립니다(`.github` 포함).
2. Settings → Pages → Source: `Deploy from a branch`, Branch: `main` / `/ (root)`. `https://earlgreypie.github.io/MOBICAT_concert/join` 이 열리면 됩니다.
3. Settings → Actions → General → Workflow permissions: `Read and write permissions`(기한 지난 첨부 지우기에 필요).

## 연주회마다

1. 앱 `연주회 편집 → 포스터로 배포 ↗ → 링크로 배포` 에서 `업로드용 묶음 만들기…` 로 파일을 만듭니다. 이름(`기한_회차_첫날.mocat`)을 바꾸지 않습니다.
2. 이 저장소 Releases → `Draft a new release` → 태그는 아무거나(예: `2026-09-26-hangawi`), 제목은 연주회 이름, 파일을 첨부하고 `Publish release`. 초안(draft)은 앱이 읽지 않습니다.
3. 앱의 `공지 문구 복사` 로 링크를 공지에 붙입니다. 여러 날 공연은 `지난 회차에 더하기` 로 만든 다른 날 파일을 같은 Release 에 더 첨부합니다 — 링크는 그대로입니다.

## 지우기

- 앱은 기한(마지막 날 다음 날)이 지난 첨부를 무시합니다.
- `.github/workflows/prune-expired.yml` 이 매주 월요일 09:00(한국 시각)에 기한 지난 첨부를 지웁니다. Actions 탭에서 `Run workflow` 로 바로 돌릴 수도 있습니다.
- 커밋으로 올리지 않습니다 — 지워도 기록에 남습니다.

## 안전

- 묶음은 회차 암호로 잠겨 있고, 암호는 링크의 `#` 뒤에만 있어 GitHub 로 가지 않습니다. 겉에는 제목 · 날짜 · 시작 시각 · 기한만 보입니다.
- 안의 묶음은 주최자 서명이 있어야 하고, 관객 앱은 그 회차에서 처음 받은 서명과 같은 것만 적용합니다.
