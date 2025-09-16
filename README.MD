
# Intobiz.io Envoy GRPC Proxy

Proxy set up for main intobiz gRPC backend



## Related

[Envoy proxy](https://www.envoyproxy.io/)  
[Docker](https://www.docker.com/)


## Installation

Pull official envoy docker image

```bash
    docker pull envoyproxy/envoy:<version>
```
    

Clone the repo locally    
```
    git clone https://github.com/g00day/IntobizGRPCProxy.git
```

Run the set up with docker in the set up directory
```
docker run -d -p 8080:8080 --network intobiz_shared_network -v "<path-to-proxy>IntobizGRPCProxy/envoy.yaml":/etc/envoy/envoy.yaml envoyproxy/envoy:<version>
```

! **Defaultly** the docker network where the main backend is runned is _intobiz_shared_network_.  
But if you have another network where all relevant backends are being runned replace it with:

```
docker run -d -p 8080:8080 --network <YOUR NETWORK NAME> -v "<path-to-proxy>IntobizGRPCProxy/envoy.yaml":/etc/envoy/envoy.yaml envoyproxy/envoy:<version>
```
## Feedback

If you have any feedback, please reach out to us at dgood4133@gmail.com

