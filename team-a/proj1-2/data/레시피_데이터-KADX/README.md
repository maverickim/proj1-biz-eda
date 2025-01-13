## 데이터명 : 레시피 (요리 난이도, 요리시간, 사용 재료/양념 수 포함)
* 회원 및 만개의레시피에서 등록한 레시피 데이터
* 컬럼 정보 : 레시피 일련 번호, 레시피 제목, 요리명, 등록자 ID, 조회수, 추천수, 요리방법별명, 요리인분명, 요리난이도명 등 18개 컬럼



#### 출처

* KADX 농식품 빅데이터 거래소
  * 제공처 : 만개의레시피 (https://www.10000recipe.com/)
  * 데이터마켓 > 소비
  * https://kadx.co.kr/opmk/frn/pmumkproductDetail/PMU_6d212747-8bd4-42c2-bc55-60bc636d6121/5



#### 기간

* 2022년 ~ 2024년 일부



#### 데이터 명세

| no | pk | type |  nameEn  | nameKo |
| ----- | ----- | ----- | ----- | ----- |
| 0 | Y | NUMBER(40)	| RCP_SNO | 레시피일련번호 |
| (제거) | N | VARCHAR(200) | RCP_TTL | 레시시제목 |
| 1 | N | VARCHAR(40) | CKG_NM | 요리명 |
| (제거) | N | VARCHAR(32) | RGTR_ID | 등록자ID |
| (제거) | N | VARCHAR(64) | RGTR_NM | 등록자명 |
| 2 | N | NUMBER(11) | INQ_CNT | 조회수 |
| 3 | N | NUMBER(11) | RCMM_CNT | 추천수 |
| 4 | N | NUMBER(11) | SRAP_CNT | 스크랩수 |
| 5 | N | VARCHAR(200) | CKG_MTH_ACTO_NM | 요리방법별명 |
| 6 | N | VARCHAR(200) | CKG_STA_ACTO_NM | 요리상황별명 |
| 7 | N | VARCHAR(200) | CKG_MTRL_ACTO_NM | 요리재료별명 |
| 8 | N | VARCHAR(200) | CKG_KND_ACTO_NM | 요리종류별명 |
| 9 | N | VARCHAR(4000) | CKG_IPDC | 요리소개 |
| 10 | N | VARCHAR(4000) | CKG_MTRL_CN | 요리재료내용 |
| 11 | N | VARCHAR(200) | CKG_INBUM_NM | 요리인분명 |
| 12 | N | VARCHAR(200) | CKG_DODF_NM | 요리난이도명 |
| 13 | N | VARCHAR(200) | CKG_TIME_NM | 요리시간명 |
| (제거) | N | CHAR(14) | FIRST_REG_DT | 최초등록일시 |
| (제거) | N | VARCHAR(200) | RCP_IMG_URL | 레시피 이미지URL (2024년만) |
| 14 (추가) | N | VARCHAR(200) | MATERIAL_CNT | 재료 수 |
| 15 (추가) | N | VARCHAR(200) | SEASONING_CNT | 양념 수 |



#### 파일 목록

* recipe_coll.csv : 2022년 ~ 2024년 데이터 수집 및 병합 데이터. 불필요 컬럼 삭제
* recipe_preproc.csv : 전처리 데이터. 'recipe_coll.csv' 에서 결측치 제거
* recipe_postproc.csv : 가공 데이터. 'recipe_preproc.csv' 에서 재료수, 양념수 추가



* TB_RECIPE_SEARCH-220701.csv : 2022년 데이터 원본

* TB_RECIPE_SEARCH-20231130.csv : 2023년 데이터 원본

* TB_RECIPE_SEARCH_241226.csv : 2024년 데이터 원본



* TB_RECIPE_SEARCH-220701-utf8.csv : 2022년 데이터. 불필요 문자 삭제. utf8로 변경

* TB_RECIPE_SEARCH-20231130-utf8.csv : 2023년 데이터 원본. 불필요 문자 삭제. utf8로 변경

* TB_RECIPE_SEARCH_241226-utf8.csv : 2024년 데이터 원본. 불필요 문자 삭제
