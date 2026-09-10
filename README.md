<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&amp;color=EAF4EF&amp;height=150&amp;text=From%20Data%20to%20Interface&amp;fontSize=34&amp;fontColor=234B3C&amp;desc=FRONTEND%20DEVELOPMENT%20%20%20DATA%20CURIOSITY&amp;descSize=12&amp;fontAlignY=45&amp;descAlignY=70" width="100%" alt="From Data to Interface — Frontend Development, Data Curiosity" />

<h1>임규영</h1>

<p><strong>Frontend Developer · 데이터가 화면이 되는 과정에 관심이 있습니다.</strong></p>

<p>
  React와 TypeScript로 인터페이스를 만들고,<br />
  복잡한 처리 결과를 사용자가 이해하고 판단할 수 있는 형태로 옮깁니다.
</p>

<p><strong>현재 SSAFY Data Track 교육 중</strong></p>

<p>
  <img src="https://img.shields.io/badge/React-234B3C?style=flat-square&amp;logo=react&amp;logoColor=white" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-234B3C?style=flat-square&amp;logo=typescript&amp;logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/TanStack_Query-234B3C?style=flat-square&amp;logo=reactquery&amp;logoColor=white" alt="TanStack Query" />
  <img src="https://img.shields.io/badge/Python-234B3C?style=flat-square&amp;logo=python&amp;logoColor=white" alt="Python" />
</p>

<p>
  <a href="#profile-education">Education</a> ·
  <a href="#profile-projects">Projects</a> ·
  <a href="#profile-toolkit">Toolkit</a>
</p>

</div>

<br />

화면에 나타나는 결과뿐 아니라, 그 결과가 만들어지는 과정에도 관심이 있습니다.
프론트엔드를 중심에 두고 데이터가 수집·처리되어 사용자에게 도달하는 흐름을 이해하려고 합니다.

그 관심은 **처리 중인 상태를 어떻게 알릴지, 실패했을 때 무엇을 안내할지,
결과를 어떤 근거와 함께 보여줄지**를 고민하는 일로 이어집니다.

<br />

<a name="profile-education"></a>

## Education

| 시점 | 기관 · 과정 | 상태 |
| :--- | :--- | :--- |
| **현재** | **SSAFY · Data Track** | 교육 중 |
| **2026.08** | **세종대학교 · 소프트웨어학과** | 학사 졸업 |

프론트엔드 프로젝트 경험을 바탕으로, 데이터 처리에 대한 이해를 넓혀가고 있습니다.

<br />

<a name="profile-projects"></a>

## Selected Projects

### 01 / It's Mine

**AI 기반 분실물 매칭 서비스**  
`2026 캡스톤 디자인` · `팀 프로젝트` · `Frontend 담당`

이미지와 텍스트로 분실물과 습득물을 매칭하는 서비스입니다.
AI 작업이 시작되는 순간부터 사용자가 결과를 비교하고 판단하는 순간까지의 프론트엔드를 담당했습니다.

- **비동기 처리 흐름** — 작업 상태를 폴링하고, 진행·대기·실패·완료에 맞는 화면을 연결했습니다.
- **이미지 후보 선택** — 사진이 없는 검색 흐름에서 서버가 수집한 후보 이미지를 비교·선택하는 UI를 구현했습니다.
- **매칭 근거 표현** — 텍스트·이미지별 점수와 AI 설명을 함께 보여주고, 모바일 캐러셀과 데스크톱 비교 화면을 구성했습니다.

`React` `TypeScript` `TanStack Query` `Zustand` `Tailwind CSS`

<details>
<summary><strong>설계와 구현 자세히 보기</strong></summary>

<br />

**작업 상태에 따른 폴링 제어**

완료·실패 등 종료 상태에서는 폴링을 중단하고, 사용자 확인이 필요한 특정 단계에서는 조건에 따라 일시 정지하도록 구성했습니다.
진행 식별자와 선택 정보는 `sessionStorage`에 보존했습니다.

**상태 관리의 역할 분리**

TanStack Query로 작업 상태·후보·매칭 결과를 조회하고,
Zustand로 사용자 선택과 진행 정보를 관리했습니다.

**인증과 테스트**

OAuth 인증 흐름과 API 연동을 담당했습니다.
Vitest·Testing Library 테스트 코드와 Playwright E2E 테스트를 구성했습니다.

> 담당 범위는 프론트엔드 UI/UX와 API 연동입니다.
> AI 모델 개발·학습과 백엔드 검색 로직은 다른 팀원이 담당했습니다.

</details>

<!-- It's Mine의 공개 가능한 실제 저장소 URL을 확인한 뒤 Repository 링크를 추가하세요. -->

<br />

### 02 / Sejong ZupZup

**지도 기반 캠퍼스 분실물 서비스**  
`팀 프로젝트` · `Frontend 참여`

세종대학교 구성원이 분실물을 등록하고 찾을 수 있도록 돕는 서비스입니다.
여러 단계의 입력을 하나의 등록 흐름으로 연결하는 프론트엔드 구현에 참여했습니다.

- **다단계 등록 폼** — 라우팅 기반 단계 이동과 등록 상태 관리를 구현했습니다.
- **입력과 업로드** — 입력 검증, 이미지 업로드, FormData 기반 API 연동을 다뤘습니다.
- **테스트 코드** — MSW로 API 응답을 모킹하고 Vitest 기반 UI·훅 테스트 코드를 작성했습니다.

`React` `TypeScript` `Zustand` `MSW` `Vitest`

[Repository ↗](https://github.com/greedy-team/zup-zup-fe)

<br />

<a name="profile-toolkit"></a>

## Toolkit

| 영역 | 사용 기술 |
| :--- | :--- |
| **Frontend** | React · TypeScript · JavaScript · Tailwind CSS · Vite |
| **State & Forms** | TanStack Query · Zustand · React Hook Form · Zod |
| **Testing** | Vitest · Testing Library · MSW · Playwright |
| **Problem Solving** | Python · Java |

**Learning / Data Processing**  
이미지·텍스트 전처리와 특성 추출, 처리 결과를 이해하기 쉽게 표현하는 방법을 공부하고 있습니다.

<br />

---

<p align="center">
  <a href="https://github.com/greedy-team">GREEDY</a> ·
  <a href="https://github.com/gxuoo/Algorithm">Algorithm — 풀이와 복습 기록</a>
</p>
