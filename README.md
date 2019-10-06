# 2019 서울 인공지능 챗봇톤 - [[link](https://www.ai-lab.kr/post/2019-chatbothon)]
> `2019. 10. 09` 9:00 ~ 21:00 서울창업허브 대강당

## 1. 아이디어
## 2. 주요 기능

## 3. 사용 스택
- [Google Dialogflow](https://cloud.google.com/dialogflow/)
- [dialogflow-web-v2](https://github.com/mishushakov/dialogflow-web-v2)
- Vue.js


## 4. Tip
- 채팅에 따른 자동 스크롤
```vue
Vue.nextTick(function () {
    var div = document.getElementById("chat-content");
    div.scrollTop = div.scrollHeight;
});
```