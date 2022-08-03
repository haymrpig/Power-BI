# Power BI 기초

## 목차

1. Power BI
   - Power BI의 종류
   - Power BI Desktop의 작업 프로세스
   - 데이터에 따른 시각화 개체 선택하기

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

![image-20220803210058144](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803210058144.png)



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

    ![image-20220803210724201](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803210724201.png)

  - **홈 - 데이터 가져오기** 탭을 누르면 가져올 수 있는 데이터 종류를 선택할 수 있다. 

    나는 엑셀 파일을 가져올 것이므로 **Excel 통합 문서**를 선택!

    ![image-20220803210830580](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803210830580.png)

  - 원하는 파일을 선택하면 파일 안의 각종 데이터를 선택하여 가져올 수 있는 것 같다.

    모두 사용할 것이므로 전체 체크!

    ![image-20220803211032722](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803211032722.png)

  - 화면 오른쪽에 필드에 데이터가 추가된 것을 확인할 수 있다. (빨간색 체크 표시)

    ![image-20220803211417300](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803211417300.png)

### 2-2. 데이터 전처리

- **실습**

  - **홈 - 데이터 변환**을 클릭하면 **Power Query 편집기**가 나온다

    ![image-20220803211830641](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803211830641.png)

  - **열 삭제하기**는 삭제하고자 하는 필드명 위에서 **마우스 우클릭 - 제거** 선택

  - **필요한 열 제외하고 삭제**는 ctrl로 필요한 필드들을 선택해주고 **마우스 우클릭 - 다른 열 제거** 선택

  - **열에서 필요없는 값은 필터링**을 통해 제거한다.

    **필드명 우측에 화살표를 클릭하고 제거할 값 체크해제**

    (아래 사진의 경우 null값을 제거한 것)

    ![image-20220803212219147](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803212219147.png)

  - **열 분할**은 해당 필드가 나누고 싶은 여러 값으로 이루어진 경우에 사용한다. 

    예를 들어, 아래 사진처럼 숫자와 영문을 나누고 싶을 때는

    **우클릭 - 열 분할 - 구분 기호 기준**을 선택하여 분할한다.

    ![image-20220803212632342](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803212632342.png)

    **옵션을 체크해주고 확인을 누른다.**

    ![image-20220803212740990](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803212740990.png)

    아래와 같이 열이 분할된 것을 알 수 있다.

    ![image-20220803212923695](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803212923695.png)

  - **열 병합**은 변환 탭 또는 열 추가 탭에서 확인할 수 있는데, 

    **변환 탭의 경우에는 기존 열을 없애고 새로 합친 열**만 남긴다.

    **열 추가 탭의 경우에는 기존 열을 남겨두고 새로 합친 열**을 만든다.

    또한 **병합할 열은 선택한 순서대로 합**쳐진다.

    ![image-20220803213913302](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213913302.png)

    ![image-20220803213940135](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213940135.png)

  - 만약 수행한 결과가 맘에 들지 않으면 모든 변경사항에 대한 기록이 남아있으므로 **X표시로 되돌리기**를 할 수 있다.

    ![image-20220803213049259](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213049259.png)

  - **데이터 타입 변경**은 **필드명 좌측을 클릭**하여 변경 가능하다.

    ![image-20220803213236807](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213236807.png)

  - **필드 값 바꾸기**는 **우클릭 - 값 바꾸기**를 통해서 진행할 수 있다.0

    ![image-20220803213521615](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213521615.png)

    ![image-20220803213540990](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213540990.png)

    ![image-20220803213615584](C:\Users\Administrator1\AppData\Roaming\Typora\typora-user-images\image-20220803213615584.png)

    

    