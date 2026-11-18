# 따릉이 패스파인더: 공공자전거 맞춤 관광코스 추천 서비스

> 서울 관광 명소 주변에서 따릉이로 둘러볼 수 있는 문화시설 코스를 추천하는 웹 서비스

| 항목 | 내용 |
|---|---|
| 기간 | 2024.06 – 2024.07 |
| 과정 | 아시아경제 「빅데이터 기반 비즈니스 모델 맞춤형 AI솔루션 개발」 1차 프로젝트 |
| 팀 | 4인 팀 · **정영균(팀장)** |
| 결과 | 문화데이터 공모전 출품 |
| 기술 | Python, Pandas, Django, Selenium, JavaScript, HTML/CSS |

<br>

## 문제
따릉이 앱은 대여·반납 중심이라 주변 문화시설을 엮은 코스를 알려주지 않습니다. 관광객이 많은 지역에서 자전거로 둘러볼 수 있는 문화·관광 코스를 추천하는 것을 목표로 했습니다.

## 내 역할 (팀장)
- 프로젝트 목표 설정, 일정과 위험 요소 관리, 팀원 역할 분담
- 코스 추천 알고리즘 개발과 알고리즘 설계도 작성
- UI/UX와 웹 서비스 구현, 최종 발표

## 접근
1. **데이터 정리**: 따릉이 대여소, 관광지, 문화시설 등 공공데이터 8종 3,358건을 모아 하나의 시설 데이터로 정제 (문화시설 약 1,120곳)
2. **평점 수집**: Selenium으로 구글 지도에서 시설별 평점을 수집하고, 평점이 없는 시설은 제외
3. **거리 계산**: Haversine 공식으로 대여소–문화시설 간 거리를 계산하고 Min-Max로 정규화
4. **추천**: 거리와 평점 점수를 결합해 시설을 고르고, 상위 시설을 묶어 코스로 추천
5. **서비스**: Django로 지도 기반 웹 화면 구현, 카테고리별 필터 제공

## 결과
관광 명소를 고르면 주변 대여소와 함께 둘러볼 문화시설 코스를 보여주는 웹 서비스를 완성해 문화데이터 공모전에 출품했습니다.

## 배운 점
출처가 다른 공공데이터를 하나의 기준으로 정리하고, 팀원들과 역할을 나눠 기한 안에 서비스를 완성하는 과정을 경험했습니다.

## 실행 방법
```bash
pip install django pandas selenium webdriver-manager
python manage.py migrate
python manage.py runserver
```

## 폴더 구조
```text
Publicbikes
├── config/    # Django 설정
├── rental/    # 대여소·문화시설 모델, 지도·필터 뷰, 데이터 적재 명령
├── templates/ # 화면
├── static/
└── doc/       # 발표 자료
```

## AI 활용
- ChatGPT로 코드 작성과 오류 수정

<br>

<details>
<summary><b>발표 자료 보기 (22장)</b></summary>
<br>

<img src="doc/슬라이드1.jpeg" width="770">
<img src="doc/슬라이드2.jpeg" width="770">
<img src="doc/슬라이드3.jpeg" width="770">
<img src="doc/슬라이드4.jpeg" width="770">
<img src="doc/슬라이드5.jpeg" width="770">
<img src="doc/슬라이드6.jpeg" width="770">
<img src="doc/슬라이드7.jpeg" width="770">
<img src="doc/슬라이드8.jpeg" width="770">
<img src="doc/슬라이드9.jpeg" width="770">
<img src="doc/슬라이드10.jpeg" width="770">
<img src="doc/슬라이드11.jpeg" width="770">
<img src="doc/슬라이드12.jpeg" width="770">
<img src="doc/슬라이드13.jpeg" width="770">
<img src="doc/슬라이드14.jpeg" width="770">
<img src="doc/슬라이드15.jpeg" width="770">
<img src="doc/슬라이드16.jpeg" width="770">
<img src="doc/슬라이드17.jpeg" width="770">
<img src="doc/슬라이드18.jpeg" width="770">
<img src="doc/슬라이드19.jpeg" width="770">
<img src="doc/슬라이드20.jpeg" width="770">
<img src="doc/슬라이드21.jpeg" width="770">
<img src="doc/슬라이드22.jpeg" width="770">
</details>
