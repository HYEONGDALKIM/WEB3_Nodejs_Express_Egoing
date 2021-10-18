## WEB3_Nodejs_Express_Egoing

<<<<<<< HEAD
- Express : Route, middleware 
    써드파티 미들웨어 : 남들이 만들어 놓은 미들웨어 (완전한 정의는 X)  


    - bodyParser
        - npm install body-parser
        - var bodyParser = require('body-parser')
        - app.use(bodyParser.urlencoded({ extended: false }))
        - 기본 express에 포함되었음 

    - Compression(압축)
        - npm install compression --save
        - var compression = require('compression');
        - app.use(compression());