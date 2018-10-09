build:
	protoc -I. --go_out=plugins=micro:$(GOPATH)/src/github.com/shippy/consignment-service \
		proto/consignment/consignment.proto
    
	go build
	docker build -t consignment-service .

run:
    docker run -p 50051:50051 consignment-service

