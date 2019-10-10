# 2019 서울 인공지능 챗봇톤 - [[link](https://www.ai-lab.kr/post/2019-chatbothon)] [[발표자료](https://docs.google.com/presentation/d/1WWwFOE-6w_0H8LiiOYaRa6_OUF1am0VseD3L3GtZiIQ/edit#slide=id.p)] 
> `2019. 10. 09 / 9:00 ~ 21:00 / 서울창업허브 대강당`

[Demo](https://onele-dev-5.firebaseapp.com)

## 0. 팀원
- 이철수
- 강중석
- 윤이건
- 이용재
- 주보화

## 1. 아이디어
> 시민 편의성을 위한 딥러닝 형태소 분석 기반의 서울시 챗봇 - `봇다리`
- 다한콜센터의 하룰 상담 20,000건 중 10%는 혼인신고, 자동차 등록, 출생, 국적 취득 등 문서작성과 관련되어 있음

## 2. 주요 기능
![](src/assets/usage.gif)
1. 상담 주제와 관련된 문서 다운로드 기능
2. 딥러닝 기반의 형태소 분석으로 성능 개선
  - ETRI의 언어모델(KorBERT) 사용하여 구글 언어모델보다 우수한 성능 확보
  - 카카오 Khaii를 이용해 Dialogflow 학습방식 개선(T-Score:97.11%)
3. 120 콜센터 주요질의를 정확히 판단 후 응대
4. 챗봇 접근성과 사용성 개선
  - 다양한 구어체 인식
  - 음성인식 기능
  - 응답 결과에 대한 TTS 제공
  - -> 시용성의 증가로 이어질 수 있음!
    - 반복질문에 대한 답변이 가능함으로 콜센터 응대 채널 분산
- `친근함`, `접근성`, `정확함`, `용이성`, `깔끔함`, `쉬움`


## 3. 사용 스택
- [Google Dialogflow](https://cloud.google.com/dialogflow/)
- [dialogflow-web-v2](https://github.com/mishushakov/dialogflow-web-v2)
- Vue.js