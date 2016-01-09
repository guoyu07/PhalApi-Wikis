#PhalApi - A light-weight PHP framework for API  - V1.3.2
  
#[PhalApi](https://github.com/phalapi/phalapi)  

#Welcome to use PhalApi!
PhalApi is a light-weight framework focus on how to develop API faster and simple.
If you have any questions, please feel free to contact us with email(chanzonghuang@gmail.com), or create an issue (https://github.com/phalapi/phalapi/issues)
   
You can use PhalApi to develop APIs very fastly and easily for Android/iOS/Windowns/Website/H5, but also build microservice/web services/RESTful for big data. 
Besides, you will explore Agile development, TDD, auto-generation etc. on the way to emergent design.  
There is more than I can say. Just enjoy it!  
  
> PhalApi is created from China since 2015, and we will try out best to make it clear how to use it smootly to everyone.   

#Install
+ *download lastest stable version from release branch*
+ *PhalApi need PHP >= 5.3.3*
  
After unpack PhalApi on your server, you can visit:
```
http://localhost/path/to/PhalApi/Public/demo/

// output
{
    "ret": 200,
    "data": {
        "title": "Default Api",
        "content": "PHPer您好，欢迎使用PhalApi！",
        "version": "1.1.0",
        "time": 1422779027
    },
    "msg": ""
}
```
  
#Demo online
```
//default api
http://demo.phalapi.net/

//api with params
http://demo.phalapi.net/?service=Default.Index&username=oschina

//illegal api
http://demo.phalapi.net/?service=Demo.None
{
    "ret": 400,
    "data": [],
    "msg": "非法请求：服务Demo.None不存在"
}
```
  
#[COOL!] Auto-generated API documents online
Here is a demo,
```
http://demo.phalapi.net/demo/checkApiParams.php
```
![mahua](http://7qnay5.com1.z0.glb.clouddn.com/20150613.png)

#[TOP!] SDK base on DSL
We can request api like:
```
PhalApiClientResponse response = PhalApiClient.create()
       .withHost("http://demo.phalapi.net/")
       .withService("Default.Index")          //service
       .withParams("username", "dogstar")     //params
       .withTimeout(3000)                     //timeout
       .request();
```
  
Curently, we provide:
 + JAVA SDK 
 + Objective-c SDK
 + PHP SDK
 + C# SDK
 + JS SDK
   
#Structure
```
.
│
├── PhalApi         // PhalApi framework, you can upgrade it in the furture
│
│
├── Public          // public visit
│   └── demo        // Demo entrance
│
│
├── Config          // common configs include app.php/sys.php/dbs.php, ect
├── Data            // common data
├── Language        // common translation
├── Runtime         // runtime log
│
│
└── Demo            // Demo
    ├── Api             // Api
    ├── Domain          // Domain
    ├── Model           // Model
    └── Tests           // PHPUnit tests

```
  
#Join us!
Welcome to join us to do something cool!

#Changelog
[changelog](http://www.phalapi.net/wikis/%5B5.6%5D-%E6%9B%B4%E6%96%B0%E6%97%A5%E8%AE%B0.html)