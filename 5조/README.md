[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FDataScience-Lab-Yonsei%2F9th_EDA%2Ftree%2Fmain%2F5%25EC%25A1%25B0%2Fhit-counter&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
![GitHub repo size](https://img.shields.io/github/repo-size/DataScience-Lab-Yonsei/9th_EDA)



## 교통(일별 지하철 역별, 노선별 승하차 인원, 버스 노선, 정류장별 승하차 인원 등 교통 관련 데이터)
#### 참여자 : 송규원, 김현동, 남승우, 심은조, 유희조, 이성균
#### EDA 프로젝트 자료 소개
> * Dataset
>   * [CARD_SUBWAY_MONTH_201501.csv - CARD_SUBWAY_MONTH_202211.csv](https://data.seoul.go.kr/dataList/OA-12914/S/1/datasetView.do) : 2015년 1월 - 2022년 11월 지하철 호선별, 역별 승하차 인원 데이터
>   * [BUS_STATION_BOARDING_MONTH_201501.csv - BUS_STATION_BOARDING_MONTH_202212.csv](https://data.seoul.go.kr/dataList/OA-12912/S/1/datasetView.do) : 2015년 1월 - 2022년 12월 버스정류장별, 노선별 승하차 인원 데이터
>   *
>   * [시간대별 지하철 승하차 인원.csv](<strong>고쳐야함</strong>)
> * 5조 EDA 발표자료 : [5조/EDA_5조_발표자료.pdf](https://github.com/DataScience-Lab-Yonsei/9th_EDA/blob/main/5%E1%84%8C%E1%85%A9/EDA_5%EC%A1%B0_%EB%B0%9C%ED%91%9C%EC%9E%90%EB%A3%8C.pdf)
> * 5조 EDA 최종 코드 :
>   * [EDA_5조_코드.ipynb](github code-url) : 데이터 수집 - 전처리(크롤링 포함) - t-test - 시각화 포함 코드
<br>



## EDA 프로젝트 요약

1. 데이터 소개

        - CARD_SUBWAY_MONTH_201501.csv - CARD_SUBWAY_MONTH_202211.csv : 2015년 1월 - 2022년 11월 지하철 호선별, 역별 승하차 인원 데이터
        - BUS_STATION_BOARDING_MONTH_201501.csv - BUS_STATION_BOARDING_MONTH_202212.csv : 2015년 1월 - 2022년 12월 버스정류장별, 노선별 승하차 인원 데이터
   
2. 데이터 전처리

        - 공개입찰을 통한 부역명 제외 -> 주역명 사용
        - Papago를 통한 지하철 역명 영문명 변환
 
3. 분석 방법 및 결과
    
        (1) 할로윈의 이태원
                - Dataset 중 승하차 인원이 많은 6개 역 중, 할로윈 직전 토요일의 승하차 인원 추출 비교
                - 이태원역은 7개 역중 승하차 인원이 많지 않은 편이었지만, 그렇지 않은 토요일에 비해, 할로윈 직전 토요일 승하차 인원에 유의미한 차이를 보임
                - 유의미한 차이를 보인 역 중 잠실역이 존재, 그러나 지형적인 특성 상 사고 사례가 드물었음
        (2) 카카오톡 먹통 사태
                - Dataset 중 Kakao 서버 오류 일주일, 하루 전-후 승하차 인원과 당일 승하차 인원 비교
                - 시각화 단계에서 Kakao 서버 오류 당일 승하차 인원을 특징짓지 못할 정도로 비슷한 양상을 보임
        (3) 신설 노선 개통
                - 9호선 2단계 - 3단계, 우이-신설선, 신림선 개통 전, 후 인접 기존 환승역 승하차 인원 변화 추이 비교
                - 간선노선(9호선) 신설 개통과 달리 지선노선(우이-신설선, 신림선) 개통 후 인접 기존 환승역 승하차 인원이 유의미한 증가 or 감소 추세를 보임
        (4) 경기버스 입석 금지
                - 이태원 사고 직후 경기버스 입석 금지 정책 시행 전-후 승하차 인원 수 비교
                - 정책 이후 승하차 인원 수의 유의미한 변화 확인 불가
        (5) 연세로 차 없는 거리 해제
                - 차 없는 거리 해제 정책 이전, 이후 버스 승하차객 변화 추이 확인
                - 정책 이전과 비교해 유의미한 차이가 있었으나, 정책 목적인 상권 활성화와의 연관성 파악 불가
    
4. 결론

        - 대중교통 승하차 인원을 다양하게 분석해, 피상적인 데이터를 통한 유의미한 결론 분석 가능
        - 같은 Dataset을 활용해 다양한 방향으로 결론 도출 가능
        - 위와 같은 Dataset을 활용해 실생활에 유용하고 안전한 방안 찾아낼 수 있음
    
5. 아쉬운 점
    
        - 경기도 버스 데이터의 경우 월별 데이터만 제공, 일별 데이터를 제공받았을 경우 더 정확한 정책 비교 가능했을 것임
        - 연세로 차 없는 거리 직후 버스 승하차 승객 수 변화를 통한 상권 활성화 연관성 파악 어려움, 장기적인 방향으로 분석해야 할 것임
        - 교통카드 태그 데이터로 인한 승하차객 수만 파악 가능, 환승 데이터를 확보했다면 더욱 정확한 추이 비교 가능 
        - 승하차 데이터만으로 승객의 정확한 행방 알수 없음 

<br>



 ## 각 팀원의 역할
 
|이름|활동 내용| 
|:---:|:---| 
|김현동| -지하철역별 승하차 인원 데이터를 활용, 토요일별 주요 역 승하차객 변화 추이 비교, 가설 설정<br> -비교한 값들에 대해 t검정, barplot 시각화<br>프로젝트 발표| 
|남승우| -지하철역별 승하차 인원 데이터 활용, 기존 노선에 대한 신설 노선의 영향력 비교, 가설 설정<br> -신설 노선 개통 전후 승하차객 변화 추이 Lineplot 시각화<br> -Dataset 전처리|
|심은조| -시간대별 대중교통 사용 인원 수 활용, Kakao 먹통 사태의 대중교통 사용량 영향 비교, 가설 설정<br> -가설 설정, 비교한 값들에 대한 시간대별 Lineplot 시각화| 
|유희조| -경기버스 입석금지 정책이 버스 사용자 수에 미친 영향 가설 설정<br> -가설 설정, 분석한 값들에 대한 boxplot 시각화| 
|이성균| -연세로 차 없는 거리 시행이 인근 버스 승하차객 변화에 미친 영향 분석, 가설 설정<br>분석한 값들에 대한 노선별 Lineplot 시각화| 
<br/>



## tree 
```bash
├── Dataset
│   ├── 서울시_대중교통_수단별_이용_현황(2017.11~2019.5)_버스.csv
│   ├── 서울시_대중교통_수단별_이용_현황(2017.11~2019.5)_철도.csv
│   ├── 할로윈의 이태원
│       ├── CARD_SUBWAY_MONTH_201510.csv
│       ├── CARD_SUBWAY_MONTH_201610.csv
│       ├── CARD_SUBWAY_MONTH_201710.csv
│       ├── CARD_SUBWAY_MONTH_201810.csv
│       ├── CARD_SUBWAY_MONTH_201910.csv
│       ├── CARD_SUBWAY_MONTH_202010.csv
│       ├── CARD_SUBWAY_MONTH_202110.csv
│       └── CARD_SUBWAY_MONTH_202210.csv
│   ├── 카카오톡 먹통사태
│       └── 서울교통공사_1_8호선 역별 일별 시간대별 승객유형별 승하차인원_20221130.csv
│   ├── 경기버스 입석금지
│       ├── 2210_남양주_1700,2000,7007.csv
│       ├── 2210_수원_3000, 3002, 3007.csv
│       ├── 2210_용인_5001, 5002A, 5002B.csv
│       ├── 2210_용인_5003A, 5003B.csv
│       ├── 2210_화성_6002, 6004.csv
│       ├── 2210_화성시_1006, 4403, 6001.csv
│       ├── 2212_남양주_1700,2000,7007.csv
│       ├── 2212_수원_3000, 3002, 3007.csv
│       ├── 2212_용인_5001, 5002A, 5002B.csv
│       ├── 2212_용인_5003A, 5003B.csv
│       ├── 2212_화성_6002, 6004.csv
│       └── 2212_화성시_1006, 4403, 6001.csv
│   └── 연세로 차 없는 거리
│       ├── BUS_STATION_BOARDING_MONTH_202207.csv
│       ├── BUS_STATION_BOARDING_MONTH_202208.csv
│       ├── BUS_STATION_BOARDING_MONTH_202209.csv
│       ├── BUS_STATION_BOARDING_MONTH_202210.csv
│       ├── BUS_STATION_BOARDING_MONTH_202211.csv
│       └── BUS_STATION_BOARDING_MONTH_202212.csv
│       
│
├── 송규원
│   └── dummy.txt
├── 김현동
│   ├── [0105]_Numpy_&_Pandas_9기_김현동_과제제출.ipynb
│   ├── [0110]_EDA방법론_9기_김현동_과제제출.ipynb
│   ├── [0112]_통계적사고_9기_김현동_과제제출.ipynb
│   ├── [0117]_Visualization_9기_김현동_과제제출.ipynb
│   └── [0119]_Crawling_9기_김현동_과제제출.ipynb
├── 남승우
│   ├── [0105]_Numpy_&_Pandas_9기_남승우_과제제출
│   ├── [0110_]EDA방법론_9기_남승우_과제제출
│       ├── df_bus.ipynb
│       └── df_subway.ipynd
│   ├── [0112]_통계적사고_9기_남승우_과제제출
│       ├── df_line.csv
│       ├── df_line.ipynb
│       ├── df_new_line_subway.ipynb
│       └── df_new_line_subway_st.ipynd
│   ├── [0117]_Visualization_9기_남승우_과제제출
│       ├── [0117]_Visualization_9기_남승우_과제제출.ipynb
│       ├── df_line_csv
│       └── df_subway.csv
│   └── [0119]_Crawling_9기_남승우_과제제출
│       ├── [0119]_Crawling_9기_남승우_과제제출.ipynb
│       ├── [0119]_Crawling_9기_남승우_과제제출.csv
│       └── [0119]_Crawling_9기_남승우_과제제출_2.csv
├── 심은조
│   ├── [0105]_Numpy_&_Pandas_9기_심은조_과제제출.ipynb
│   ├── [0110]_EDA방법론_9기_심은조_과제제출.ipynb
│   ├── [0112]_통계적사고_9기_심은조_과제제출.ipynb
│   ├── [0117]_Visualization_9기_심은조_과제제출.ipynb
│   └── [0119]_Crawling_9기_심은조_과제제출.ipynb
├── 유희조
│   ├── [0105]_Numpy_&_Pandas_9기_유희조_과제제출.ipynb
│   ├── [0110]_EDA방법론_9기_유희조_과제제출.ipynb
│   ├── [0112]_통계적사고_9기_유희조_과제제출.ipynb
│   ├── [0117]_Visualization_9기_유희조_과제제출.ipynb
│   └── [0119]_Crawling_9기_유희조_과제제출.ipynb
├── 이성균
│   ├── [0105]_Numpy_&_Pandas_9기_이성균_과제제출.ipynb
│   ├── [0110]_EDA방법론_9기_이성균_과제제출.ipynb
│   ├── [0112]_통계적사고_9기_이성균_과제제출.ipynb
│   ├── [0117]_Visualization_9기_이성균_과제제출.ipynb
│   └── [0119]_Crawling_9기_이성균_과제제출.ipynb
│
├── EDA_5조_발표자료.pdf
├── EDA_5조_최종_발표자료.pdf
├── EDA_5조_코드
│
└── README.md
``` 
