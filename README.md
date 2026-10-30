# 송도해상케이블카 광고매체 안내

사진과 광고매체 정보를 제공하는 인터랙티브맵입니다.

## 게스트 / 관리자
- 게스트: https://budsign-hub.github.io/songdoad/ 에서 로그인 없이 열람
- 관리자: 지도 화면 우측 상단 [관리자] → 비밀번호 로그인 → 사진·판매상태·광고료·메모·공간 이름 수정 → 상단 [변경사항 게시]
  - 게시 전 수정분은 그 브라우저에만 임시 저장됩니다.
  - 게시하면 저장소에 커밋되고, GitHub Pages가 1~2분 안에 공개 페이지에 반영합니다.

## 파일
| 파일 | 내용 |
|---|---|
| `index.html` | 페이지 (기본 데이터 내장, 비상시 대체 표시용) |
| `overrides.json` | 공개 데이터 (사진 경로·판매상태·광고료·메모·공간 이름) — 관리자 게시 시 갱신 |
| `photos/` | 현장사진 (SHA-256 파일명) |
| `admin-key.json` | 관리자 비밀번호로 암호화된 GitHub 토큰 (AES-GCM, PBKDF2-SHA256 60만 회) |

## 최초 설정 · 토큰 재설정
1. GitHub → Settings → Developer settings → Fine-grained personal access tokens → Generate new token
2. Repository access: Only select repositories → `songdoad`
3. Permissions → Repository permissions → Contents: **Read and write**
4. 사이트에서 [관리자] → (설정이 없으면 자동으로) 관리자 설정 → 토큰 + 새 비밀번호(10자 이상) 입력

토큰이 만료되면 로그인 시 재설정 화면이 열립니다. 비밀번호는 로그인 후 상단 [비밀번호 변경]에서 바꿉니다.
