# ✈️ YaKaJa !

- **개발기간** : ﻿2025.04.15 ~ 2025.04.28 (총 15일)
- **참여인원** : 5명  
- **담당업무** : 제안, 기획, 전체 디자인, 담당 기능 개발
- **개발환경** : Tomcat 8.5, Oracle DB, Eclipse, ojdbc8
- **사용도구** : ﻿draw.io
- **사용기술** : ﻿Java, JavaSwing, SHA-256

---

## 📖 개요
&nbsp;&nbsp;본 프로젝트는 여행을 계획할 때 각각의 여행지, 먹거리, 숙박 정보를 따로 찾아야 하는 번거로움을 해결하기 위해 기획되었습니다. 사용자가 한눈에 여행 일정을 구성할 수 있도록 통합적인 플랫폼을 제공하여, 불필요한 검색 과정을 줄이고 효율적으로 여행을 준비할 수 있도록 하는 데에 초점을 두었습니다.  
&nbsp;&nbsp;이를 통해 여행 계획 과정을 단순화하고, 개인 맞춤형 추천을 더해 사용자 경험을 향상시키는 것을 목표로 하였습니다. 단순한 정보 제공을 넘어, **여행 전체를 하나의 경험으로 묶어주는 서비스**를 제안하는 프로젝트입니다.

---

## 💡 기획 의도(동기)
&nbsp;&nbsp;여행을 준비할 때는 여행지, 먹거리, 숙박 정보를 각각 따로 찾아야 하는 번거로움이 존재합니다. 이 과정에서 여러 플랫폼을 오가며 정보를 수집해야 하므로 시간과 노력이 많이 들고, 통합적인 일정 관리가 어렵다는 한계가 있습니다.  
&nbsp;&nbsp;이에 본 프로젝트는 여행자가 필요한 요소들을 한 곳에서 쉽게 찾고, 연결된 경험으로 설계할 수 있도록 돕는 것을 목표로 합니다. 여행지 탐색부터 음식점 추천, 숙박 예약까지 **여행 전반을 통합 관리**할 수 있는 서비스를 제공함으로써 사용자가 보다 편리하게 여행을 계획할 수 있도록 합니다.  
&nbsp;&nbsp;즉, 단순한 정보 제공을 넘어, **여행 전체를 하나의 경험으로 묶어주는 플랫폼**을 구현하는 것이 이 프로젝트의 핵심 동기입니다.


---

## 🎯 목표 및 설계
### 🎯 목표
- 소비자들이 **경제적인 지출**을 할 수 있는 여행 플랫폼 제공  
- 넓은 카테고리를 통해 **지역 문화 활성화** 기여  
- 직접 조사하지 않아도 **다양한 여행 경험**을 손쉽게 제공  
- 여행지·먹거리·숙박을 통합 관리할 수 있는 **올인원 서비스** 구현  

### 📊 ERD & 테이블 설계
ERD 이미지 첨부 (https://drive.google.com/file/d/1kbEHif0bIhkfOeUg5ZFvOEti6dIDmlDk/view?usp=drive_link)

<details>
<summary>📷 ERD 이미지 더보기</summary>
  
<img width="463" height="580" alt="스크린샷 2025-09-28 235556" src="https://github.com/user-attachments/assets/f3db5c80-8ec4-47a8-94c9-a3fa599330b0" />


</details>

#### 주요 테이블
- **로그인/회원 관리** : `MEMBER`  
- **예약 관리** : `RESERVATION`, `RESERVATION_DETAIL`  
- **지역 데이터** : `REGION`  
- **여행 상품 데이터** : `ITEM`  


---

### 🛠️ 담당 역할
#### 1. 로그인 / 회원가입 구현 
- 회원가입 시 입력 데이터 유효성 검사 및 DB 연동  
- 로그인 세션 관리로 사용자 상태 유지  

#### 2. 메인 화면 제작
- 프로젝트 전체의 첫 진입 화면 설계 및 UI 구현  
- 직관적인 메뉴 배치 및 배너 영역 제작  

#### 3. 일정 선택 화면
- 사용자 일정 입력 및 선택 기능 개발  
- 선택한 일정에 따라 예약 정보가 DB에 저장되도록 처리  
- UI/UX 고려한 달력/드롭다운 기반 일정 선택 인터페이스 구현  

#### 4. 마지막 화면 (예약 완료 페이지)
- 예약 완료 후 사용자에게 결과 요약 정보 제공  
- 선택한 일정/상품/가격 정보 시각화  
- 메인화면 및 마이페이지로 이동 가능한 네비게이션 버튼 구성  


---

<details>
<summary>📷 화면 구성(클릭해서 보기) </summary>


|구분 | 화면 | 미리보기 |
|----------|----------|----------|
|공통| 메인화면(로그인) | <img width="633" height="860" alt="ygjlogin" src="https://github.com/user-attachments/assets/468c035d-bbaf-4925-a1cf-939730a13fac" /> |
|공통| 회원가입 | <img width="633" height="862" alt="ygjgaip" src="https://github.com/user-attachments/assets/d150cd87-8dc4-4666-ba50-f0239158626f" /> |
|공통| 유저화면 | <img width="635" height="859" alt="KakaoTalk_20250424_125426503_01" src="https://github.com/user-attachments/assets/57310e50-f497-4964-82f7-1f65e8af76ea" /> |
|공통| 일정선택 | <img width="634" height="860" alt="KakaoTalk_20250424_125426503_03" src="https://github.com/user-attachments/assets/cded27b9-8efd-4ac4-ad2d-b4bb0268c779" /> |
|유저| 지역선택 | <img width="634" height="863" alt="ygjmap" src="https://github.com/user-attachments/assets/4d0599b5-4051-4eeb-9312-56be052416ce" /> |
|유조| 여행정보 | <img width="633" height="861" alt="KakaoTalk_20250424_125426503_04" src="https://github.com/user-attachments/assets/627f3796-0519-424b-8562-36a14c1895d8" /> |
|유저| 결제하기| <img width="400" height="453" alt="image" src="https://github.com/user-attachments/assets/b7988708-66fe-44c4-ba80-412fc615cac7" /> |
|유저| 결제확인 페이지 | <img width="295" height="761" alt="KakaoTalk_20250424_131745240_01" src="https://github.com/user-attachments/assets/75f4084b-881a-4d8a-a7c8-91740302bab6" /> |
|유저| 여행일정 불러오기 | <img width="633" height="862" alt="ygjbul" src="https://github.com/user-attachments/assets/0b374359-f1cd-4f43-9df0-aeead39cef7f" /> |
|유저| 마지막 페이지 | <img width="637" height="866" alt="ygjlast" src="https://github.com/user-attachments/assets/a91d2354-d642-47e9-aba3-78e9e64db628" /> |
|관리자| 예약 현황 | <img width="1268" height="798" alt="스크린샷 2025-09-29 001912" src="https://github.com/user-attachments/assets/993617d8-0b41-4e4c-a29e-2c3d7a4fc354" /> |
|관리자| 회원 정보 | <img width="1279" height="809" alt="image" src="https://github.com/user-attachments/assets/189e9356-5622-476e-a91b-db898b3723a1" /> |
|관리자| 아이템 정 | <img width="1275" height="795" alt="image" src="https://github.com/user-attachments/assets/260cc367-f49d-48ef-9512-50f1b12e874b" /> |

</details>

---

### 🏆 성과 및 후기 
- **로그인 / 회원가입 기능 구현**  
  - 회원가입 시 입력값 검증 및 DB 연동을 통해 안정적인 사용자 관리 기능 제공  
  - 로그인 세션 관리로 사용자별 맞춤 서비스 경험 제공  

- **메인 화면 제작**  
  - 핵심 기능과 메뉴를 직관적으로 배치하여 사용자 편의성 강화  
  - 반응형 레이아웃을 적용해 다양한 기기 환경에서도 일관된 UI/UX 제공  

- **일정 선택 화면 개발**  
  - 달력/드롭다운 기반 UI를 통해 사용자가 손쉽게 일정 선택 가능  
  - 선택한 일정이 예약 DB와 연동되도록 구현하여 서비스 흐름 완성도 향상  

- **마지막 화면 (예약 완료 페이지)**  
  - 예약 결과 요약 및 시각화로 사용자가 직관적으로 결과 확인 가능  
  - 메인/마이페이지 이동 버튼 제공으로 사용자 동선 최적화  


<details>
<summary> 후기 더보기 </summary>


## ✨ 후기

- **로그인 / 회원가입 구현 경험**  
  단순히 계정을 생성하고 로그인하는 기능을 넘어서, 입력값 검증과 세션 관리 등 안정적인 사용자 인증 시스템을 구현할 수 있었습니다. 이를 통해 **보안성과 편의성을 동시에 고려해야 하는 회원 관리의 중요성**을 배웠습니다.  

- **메인 화면 제작 경험**  
  메인 화면은 사용자가 가장 먼저 접하는 서비스의 얼굴이라는 점에서, 단순한 배치가 아닌 **핵심 기능을 직관적으로 전달할 수 있는 구조**가 필요하다는 것을 깨달았습니다. 반응형 레이아웃과 직관적인 네비게이션을 통해 UX 중심의 설계를 실습할 수 있었습니다.  

- **일정 선택 화면 개발 경험**  
  사용자가 원하는 일정을 쉽게 선택할 수 있도록 달력과 드롭다운 UI를 설계했습니다. 단순 UI 구현이 아니라 DB 연동을 통해 예약 흐름이 실제 서비스로 이어지도록 구현하며, **사용자 경험과 데이터 구조의 연결성**을 체감했습니다.  

- **예약 완료(마지막) 화면 구현 경험**  
  예약 내역을 직관적으로 확인할 수 있도록 결과 요약과 버튼 동선을 설계했습니다. 단순히 결과를 보여주는 것을 넘어서 **다음 행동(메인 이동, 마이페이지 이동 등)을 자연스럽게 유도하는 UI/UX**의 중요성을 배웠습니다.  

- **종합적인 배움**  
  이번 프로젝트는 Eclipse 환경에서 진행되었으며, 단순 CRUD를 넘어서 **UI/UX 설계, DB 연동, 사용자 흐름 설계**를 직접 경험할 수 있었습니다. 특히 화면 하나하나가 독립된 기능이 아니라 **서비스 전체의 흐름 속에서 연결되어야 한다는 점**을 실감하며, 초기 설계와 사용자 중심 사고가 프로젝트 완성도에 큰 영향을 준다는 것을 배웠습니다.  


</details>

---

### 🎥 시연 자료
- [📺 시연 영상 보기](https://drive.google.com/file/d/1TLn_pS-Dg8SKAuKlLZssa4tMcJxC8bHr/view?usp=drive_link) - 관리자
- (https://drive.google.com/file/d/1OP9iLADdIWlFux0vKZnAtSsycVRSFGnS/view?usp=drive_link) - 사용
- [📑 발표 자료 (PPT)](https://drive.google.com/file/d/1sIPAWwSvjvaGObK-X6DzlWzRFNgI6WNI/view?usp=drive_link)
- [📑 발표 자료 (pdf)](https://drive.google.com/file/d/1kZ1lKXoHUVIgaIuZZHtrYHtDarcm1WW7/view?usp=drive_link)
- [📑 UML](https://drive.google.com/file/d/1SbN2PphGj1hwFAbpD1wxCA5cPfQGik-X/view?usp=drive_link)
