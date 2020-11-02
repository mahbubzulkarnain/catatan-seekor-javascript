---
description: 'Robert Griesemer, Rob Pike, and Ken Thompson.'
---

# Catatan Seekor: GOLANG

#### Conditional

#### The _if_ Statement

```go
const conditional = true
const isTrue = "text true"

if conditional {
	fmt.Println(isTrue)
}

// Output: "text true"
```

### Looping

#### The _for_ Statement

```go
input := [...] string {"t","","r","","u","","e","1","2"}

var output string
for i := 0; i < len(input); i++ {
	if input[i] == "" {
		continue
	}
	if len(output) > 3 {
		break
	}
	output += input[i]
}

fmt.Println(output) // "true"
```

### Links

* [5 Ways to Live Reloading Go Applications](https://techinscribed.com/5-ways-to-live-reloading-go-applications/)
* [Allocation efficiency in high-performance Go services](https://segment.com/blog/allocation-efficiency-in-high-performance-go-services/)
* [Awesome Docker](https://awesome-docker.netlify.app/)
* [A web framework written in Golang](https://golangexample.com/a-web-framework-written-in-golang/)
* [An Example of Using NSQ From Go](http://tleyden.github.io/blog/2014/11/12/an-example-of-using-nsq-from-go/)
* [API Resources for Go Developers](https://www.moesif.com/blog/api-guide/development/api-resources-for-go-developers/)
* [Beating JSON performance with Protobuf](https://auth0.com/blog/beating-json-performance-with-protobuf/)
* [BogoToBogo](https://www.bogotobogo.com/GoLang/GoLang_HelloWorld.php)
* [Build Web Application with Golang](https://astaxie.gitbooks.io/build-web-application-with-golang/en/)
* [Building Docker Containers for Go Applications](https://www.callicoder.com/docker-golang-image-container-example/)
* [Dasar Pemrograman Golang](https://dasarpemrogramangolang.novalagung.com/)
* [Deploying a Go application on AWS EC2](https://hackernoon.com/deploying-a-go-application-on-aws-ec2-76390c09c2c5)
* [Getting Started with Kafka in Golang](https://medium.com/@yusufs/getting-started-with-kafka-in-golang-14ccab5fa26)
* [Getting Started with Serverless Go](https://dev.to/yos/getting-started-with-serverless-go--1lff)
* [Golang & SOAP Based Services](https://levelup.gitconnected.com/golang-soap-based-services-ccc4b3e3ee2e)
* [Golang Bot](https://golangbot.com/)
* [Golang Code](https://golangcode.com/)
* [Golang Programs](https://www.golangprograms.com)
* [Gomock — unit testing made easy](https://medium.com/@duythhuynh/gomock-unit-testing-made-easy-b59a0e947ba7)
* [High Performance Go Workshop](https://dave.cheney.net/high-performance-go-workshop/dotgo-paris.html)
* [Hot Example](https://golang.hotexamples.com/)
* [How to use RegEx in GoLang](https://www.educative.io/edpresso/how-to-use-regex-in-golang)
* [Implementasi Kafka menggunakan Golang + Testing](https://medium.com/easyread/implementasi-kafka-menggunakan-golang-testing-db183e0b3c29)
* [Lambdas with GoLang — a technical guide](https://cloudnative.ly/lambdas-with-golang-a-technical-guide-6f381284897b)
* [Learn Go with Tests](https://quii.gitbook.io/learn-go-with-tests/)
* [Membangun Realtime Canvas Drawing Dengan Go, Websocket dan P5.js](https://medium.com/@wuriyantomusobar/membangun-realtime-canvas-drawing-dengan-go-websocket-dan-p5-js-672c799d3044)
* [Regular Expression to Check Indonesian MobilePhone Provider](https://edwin.baculsoft.com/2014/08/regular-expression-to-check-indonesian-mobilephone-provider/)
* [SOAP - WSDL request in Go Language](https://medium.com/eaciit-engineering/soap-wsdl-request-in-go-language-3861cfb5949e)
* [Solving the "does not support indexing" error in a Go program](https://flaviocopes.com/golang-does-not-support-indexing/)
* [Testing with GoMock: A Tutorial](https://blog.codecentric.de/en/2017/08/gomock-tutorial/)
* [Tutorial Edge](https://tutorialedge.net/course/golang/)
* [Writing Great Go Code](https://scene-si.org/2018/07/24/writing-great-go-code/)

#### Architecture

* [Clean Architecture using Golang](https://dev.to/eminetto/clean-architecture-using-golang-5791) by [Elton Minetto](https://github.com/eminetto)
* [The Clean Code Blog](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) by [Robert C. Martin \( Uncle Bob \)](https://github.com/unclebob)
* [Trying Clean Architecture on Golang](https://hackernoon.com/golang-clean-archithecture-efd6d7c43047) by [Iman Tumorang](https://github.com/bxcodec)

#### Stackoverflow

* [Assigning null to JSON fields instead of empty strings](https://stackoverflow.com/questions/31048557/assigning-null-to-json-fields-instead-of-empty-strings)
* [Docker: go get from a private GitHub repo](https://stackoverflow.com/questions/26161541/docker-go-get-from-a-private-github-repo)
* [How to pass arguments to router handlers in Golang using Gin web framework?](https://stackoverflow.com/questions/34046194/how-to-pass-arguments-to-router-handlers-in-golang-using-gin-web-framework)
* [How to use Go with a private GitLab repo](https://stackoverflow.com/questions/29707689/how-to-use-go-with-a-private-gitlab-repo)
* [gometalinter / errcheck returns a warning on deferring a func which returns a variable](https://stackoverflow.com/questions/40397781/gometalinter-errcheck-returns-a-warning-on-deferring-a-func-which-returns-a-va)
* [Remove diacritics using Go](https://stackoverflow.com/questions/26722450/remove-diacritics-using-go)

#### CI/CD

* [GolangCI](https://golangci.com/)

#### Github

* [awesome-auth](https://github.com/casbin/awesome-auth)

#### Docs

* [Golang](https://golang.org/doc/)

