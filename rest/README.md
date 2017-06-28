## ReST api


> The rest will create a new client/volume , stop/check with user response 

### client.go

- Newclient () --> creates a new client 
  ```go
  func NewClient(addr, base string) *Client {
        return &Client{addr, base}
}


- Volumeexist () --> To check whether volume exists (or) not 
 ```go
 func (r Client) VolumeExist(name string) (bool, error) {
        vols, err := r.volumes()
        if err != nil {
                return false, err
        }

        for _, v := range vols {
                if v.Name == name {
                        return true, nil
                }
        }

        return false, nil
}
```
- volume () --> to check and compare the volume names with the local host

- CreateVolume () --> to stop the volume 
 ```go 
    
    ```
    
    ``` code will be updated soon ```
