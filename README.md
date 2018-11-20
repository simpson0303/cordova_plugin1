# Cordova plugin background gps track
Cordova plugin background gps track Service With Cordova/Phonegap android application




## Master branch:
 
 ```
cordova plugin add https://github.com/simpson0303/cordova_plugin1.git
 ```
## local folder:

 ``` 
cordova plugin add cordova_plugin1 --searchpath path

```


## 1) Get Current Location
  ```
  navigator.gpstrack.getCurrentLocation(function(result){
     console.log(result.latitude + " == "+result.longitude );
   },function(e){
    console.log("Error" + e);
    });
  
  
```
## 2) Start service 

 //add service value in ServerDetails like :
  [{latitude: "",longitude: "","params1":"value","params2":"value","params3":"value","params4":"value", ......}]
 ```  
    var option = { "ServerDetails":[{latitude: "",longitude: "",  .....}],
                   "IntervalTime": 60, // Time set in second default time one min.
                   "IntervalDistance":"100", // Distance set in meter "now not working distance"
                   "ServerURL": setUrl //Server URL
                  };
          navigator.gpstrack.start(function(a){console.log("start")},function(){console.log("Error")},option);
     
 ``` 
  
## 3) Stop service 
  ```
  navigator.gpstrack.stop(function(a){console.log("stop")},function(){console.log("Error")});
  
```
simpson0303 0 1
1 0 LokeshPatel