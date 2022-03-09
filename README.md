# full-app
Express + mongoDB + React  (리액트 프로젝트 안에 빌드한 버전)


## Express(서버) 라우터와 React 라우터 둘 다 사용 할 시 

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

## ee

![img1.png]
