## WEB3_Nodejs_Express_Egoing

- 애플리케이션 레벨 미들에어 

        app.use() 및 app.METHOD() 함수를 이용해 애플리케이션 미들웨어를 앱 오브젝트의 인스턴스에 바인드하십시오.

        이때 METHOD는 미들웨어 함수가 처리하는 요청(GET, PUT 또는 POST 등)의 소문자로 된 HTTP 메소드입니다.

        next()로 인해서 순서를 결정하고 미들웨어를 몇 개 연결할 수 있다.
        
- Express : Route, middleware 

    써드파티 미들웨어 : 남들이 만들어 놓은 미들웨어 (완전한 정의는 X)  

    - bodyParser
        - npm install body-parser
        - var bodyParser = require('body-parser')
        - app.use(bodyParser.urlencoded({ extended: false }))
        - 이제는 기본 express에 포함되었음 

    - Compression(압축)
        - npm install compression --save
        - var compression = require('compression');
        - app.use(compression());

    - 정적인 파일 서비스하는 방법 
        - unsplash(저작권 X)
        - express.staic(root, [option])
        - app.use(express.static('public'));

    - 에러처리(없는 페이지)
        - app.use(function(req, res, next) {
          res.status(404).send('404! not fount');
          });
        - 오류 호출 할때 인자를 err로 주고
        - app.use(function (err, req,  res, next) {
          console.error(err.stack)
          res.status(500).send('500! Not found page')
          }); 
        - 위 코드를 호출하게끔 약속되어있다.

     - 주소체계 변경
         - 간단한 소프트웨어라도 하나의 수정에 전체코드에 많은 수정이 필요함

     - 라우터 
         - 파일로 분리 topic.js

     - 여러가지 단골 보안 이슈들을 해결해줌
       - helmet

       - npm install --save helmet

     - express Generator 

        - https://www.inflearn.com/course/node-js-express/lecture/13898?tab=curriculum

        -Express 기반의 프로젝트를 할 때 기본적으로 필요한 파일과 코드를 

         자동으로 만들어주는 앱인 Express generator를 소개합니다. 

 
     - 데이터베이스 통합
        데이터베이스를 Express 앱에 연결하는 기능을 추가하려면 앱에 포함된 데이터베이스를 위한 적절한 Node.js 드라이버를 로드해야 합니다. 이 문서에서는 Express 앱의 데이터베이스 시스템에 가장 널리 이용되고 있는 Node.js 모듈 중 다음과 같은 몇 개의 모듈을 추가 및 사용하는 방법을 설명합니다.

                Cassandra
                CouchDB
                LevelDB
                MySQL
                MongoDB
                Neo4j
                PostgreSQL
                Redis
                SQLite
                ElasticSearch
                

        - 적은 노동 >> 많은 효율 
