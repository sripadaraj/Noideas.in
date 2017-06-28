# api
Docker-volume-driver client ReSET_api 

> The api will -automatically creates/resolves and sends back the uuid  of the volume for ![docker-volume-driver](https://github.com/maheshreddy7797/docker-volume-driver) 

![REst api](https://github.com/sripadaraj/ReST_api/blob/master/IMG%20SRC/REst%20API%201%20-%202-02.jpg)
  
## get the package 

 ``` go get github.com/sripadaraj/ReST_api  ```

## usage 

 ```go
 package main

import (
  "log"
  docker-volume-driver_api "github.com/sripadaraj/ReST_api"
)

func main() {
    client := docker-volume-driver_api.NewrpcClient("http://your api server :<port>", "user", "password")
    req := &docker-volume-driver_api.CreateVolumeRequest{
        Name:              "MyVolume",
        RootUserID:        "root",
        RootGroupID:       "root",
        ConfigurationName: "base",
    }
    volume_uuid, err := client.CreateVolume(req)
    if err != nil {
        log.Fatalf("Error:", err)
    }

    log.Printf("%s", volume_uuid)
}
 ``` 
