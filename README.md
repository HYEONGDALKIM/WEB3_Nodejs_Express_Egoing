## WEB3_Nodejs_Express_Egoing

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
