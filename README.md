# full-app
Express + mongoDB + React  (리액트 프로젝트 안에 빌드한 버전)


## Express(서버) 라우터와 React 라우터 둘 다 사용 할 시 
- Express 라우터는 REST API 요청 오는 처리를 위해 사용
- React 라우터는 화면 전환을 위해 사용

```
[server.js]

// API 호출 시  ./back/routes/route 경로 코드 실행 
app.use( '/api' ,back);     

// 그 외의 호출은 react 실행
app.use( '/' ,express.static(path.join(__dirname, './front/build')));  
app.get('*', function(req,resp){
    resp.sendFile( path.join(__dirname, './front/build/index.html'))
})


```

## 설명
1. 리액트 라우터로 움직이는 home 
- ![img1](https://user-images.githubusercontent.com/30708283/157447330-d7c58a91-9469-4f15-bb00-fd2e3ecbdf93.png)

2. 리액트 라우터로 움직이는 About
- ![img2](https://user-images.githubusercontent.com/30708283/157447334-b29a64b2-e101-4f7f-a128-9168e4fa593a.png)

3. 리액트 라우터로 움직이는 API (이지만 리액트 AXIOS로 요청해서 Express 라우터로 API를 호출하는 )
- ![img3](https://user-images.githubusercontent.com/30708283/157447338-6a202583-21cd-4773-affd-68ed9f8422af.png)
