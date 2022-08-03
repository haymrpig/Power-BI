# Power BI 기초

## 목차

1. Power BI
   - Power BI의 종류
   - Power BI Desktop의 작업 프로세스
   - 데이터에 따른 시각화 개체 선택하기
2. Power BI Desktop 실습
   - 데이터 가져오기
   - 데이터 전처리
     - 열 삭제
     - 필요한 열 제외하고 삭제
     - 필요없는 값 필터링
     - 열 분열
     - 열 병합
     - 되돌리기
     - 데이터 타입 변경
     - 필드에서 특정값 필터링하여 다른 값으로 변경

# 1. Power BI 

### 1-1. Power BI의 종류

- Power BI Service
- Power BI Desktop
- Power BI Mobile

### 1-2. Power BI Desktop의 작업 프로세스

1. **데이터 가져오기**
   - 파일 (Excel, Text, CSV), DB, 온라인 서비스 Web, R 등 다양한 유형의 데이터 원본 지원
2. **데이터 정리 및 변환**
   - 파워 쿼리 편집기를 사용하여 데이터를 분석에 적합한 형태로 편집
3. **데이터 모델링**
   - 효과적으로 데이터를 분석할 수 있도록 준비
   - 관계 작성, 데이터 형식 지정, 열 기준 정렬, 분석식 작성 (DAX)
4. **데이터 시각화**
   - 다양한 시각적 개체를 사용하여 시각화 보고서 작성

### 1-3. 데이터에 따른 시각화 개체 선택하기

![image](https://user-images.githubusercontent.com/71866756/182614326-54476fd1-cc8d-47cb-bff7-1090e1b9dcf3.png)



# 2. Power BI Desktop 실습

### 2-1. 데이터 가져오기

- **Power BI Desktop에서 가져올 수 있는 데이터들**

  - **파일** : 엑셀 파일 (xlsx, xlsm), 텍스트, csv 등
  - **DB** : MSSQL, Oracle, MySQL, Azure SQL DB 등
  - **서비스** : Dynamic 365, Google Analytics, Bing, Salesforce 등
  - **기타** : Hadoop, Facebook, R/Python 스크립트, 웹, ODBC 등

  > 아직 엑셀 파일, csv, 텍스트, MySQL 정도밖에 모르겠다... 좀 더 공부해야 될듯

- **실습**

  - 이게 가장 처음 Power BI Desktop을 열었을 때의 화면이다.

    ![image](https://user-images.githubusercontent.com/71866756/182614355-b16d2cb8-d594-4dab-84d4-00008c9e2065.png)

  - **홈 - 데이터 가져오기** 탭을 누르면 가져올 수 있는 데이터 종류를 선택할 수 있다. 

    나는 엑셀 파일을 가져올 것이므로 **Excel 통합 문서**를 선택!

    ![image](https://user-images.githubusercontent.com/71866756/182614393-f5584d7b-80fd-489c-be94-e6d8666c2992.png)

  - 원하는 파일을 선택하면 파일 안의 각종 데이터를 선택하여 가져올 수 있는 것 같다.

    모두 사용할 것이므로 전체 체크!

    ![image](https://user-images.githubusercontent.com/71866756/182614413-3ef510aa-283a-48e5-ba40-1b4799b0c3a6.png)

  - 화면 오른쪽에 필드에 데이터가 추가된 것을 확인할 수 있다. (빨간색 체크 표시)

    ![image](https://user-images.githubusercontent.com/71866756/182614429-5b7c2288-0035-4a1b-8dc6-5ef34e7f2da9.png)

### 2-2. 데이터 전처리

- **실습**

  - **홈 - 데이터 변환**을 클릭하면 **Power Query 편집기**가 나온다

    ![image](https://user-images.githubusercontent.com/71866756/182614439-47720f5f-c0d8-4e00-b2b1-3d8db573179e.png)

  - **열 삭제하기**는 삭제하고자 하는 필드명 위에서 **마우스 우클릭 - 제거** 선택

  - **필요한 열 제외하고 삭제**는 ctrl로 필요한 필드들을 선택해주고 **마우스 우클릭 - 다른 열 제거** 선택

  - **열에서 필요없는 값은 필터링**을 통해 제거한다.

    **필드명 우측에 화살표를 클릭하고 제거할 값 체크해제**

    (아래 사진의 경우 null값을 제거한 것)

    ![image](https://user-images.githubusercontent.com/71866756/182614470-0f5b88b6-d7ee-4dad-aecf-40641992fdea.png)

  - **열 분할**은 해당 필드가 나누고 싶은 여러 값으로 이루어진 경우에 사용한다. 

    예를 들어, 아래 사진처럼 숫자와 영문을 나누고 싶을 때는

    **우클릭 - 열 분할 - 구분 기호 기준**을 선택하여 분할한다.

    ![image](https://user-images.githubusercontent.com/71866756/182614490-ce564b46-e2f0-4452-8282-3c007405c51e.png)

    **옵션을 체크해주고 확인을 누른다.**

    ![image](https://user-images.githubusercontent.com/71866756/182614516-73fab05c-3958-442e-bf67-1170db47f458.png)

    아래와 같이 열이 분할된 것을 알 수 있다.

    ![image](https://user-images.githubusercontent.com/71866756/182614550-e98ab010-1812-4ef7-8249-5fcb73c2033c.png)

  - **열 병합**은 변환 탭 또는 열 추가 탭에서 확인할 수 있는데, 

    **변환 탭의 경우에는 기존 열을 없애고 새로 합친 열**만 남긴다.

    **열 추가 탭의 경우에는 기존 열을 남겨두고 새로 합친 열**을 만든다.

    또한 **병합할 열은 선택한 순서대로 합**쳐진다.

    ![image](https://user-images.githubusercontent.com/71866756/182614576-5bb46a86-fd3e-4cd5-8af5-f25963279211.png)

    ![image](https://user-images.githubusercontent.com/71866756/182614591-ba369f6c-7c9a-4a1e-b094-431d2fd2160a.png)

  - 만약 수행한 결과가 맘에 들지 않으면 모든 변경사항에 대한 기록이 남아있으므로 **X표시로 되돌리기**를 할 수 있다.

    ![image](https://user-images.githubusercontent.com/71866756/182614614-0d0906e8-8edd-442d-a9a3-d6393a70752b.png)

  - **데이터 타입 변경**은 **필드명 좌측을 클릭**하여 변경 가능하다.

    ![image](https://user-images.githubusercontent.com/71866756/182614648-2bc51b11-f24b-47a9-83c9-764f6017a6a9.png)

  - **필드 값 바꾸기**는 **우클릭 - 값 바꾸기**를 통해서 진행할 수 있다.0

    ![image](https://user-images.githubusercontent.com/71866756/182614660-5301729f-2f51-4cbb-9505-e9dae936be68.png)

    ![image](https://user-images.githubusercontent.com/71866756/182614679-1c9ecfe4-c718-43ec-aae5-b2b3076b323a.png)

    ![image](https://user-images.githubusercontent.com/71866756/182614699-e33eb069-60d7-44c7-a4c0-ecc01d44da88.png)

    

    
