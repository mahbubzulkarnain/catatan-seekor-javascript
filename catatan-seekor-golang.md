---
description: 'Robert Griesemer, Rob Pike, and Ken Thompson.'
---

# Catatan Seekor: GOLANG

### Data Types

**Numeric**

```go
var iniNumeric int8     // 0 - 255
var iniNumeric int16    // 0 - 65535
var iniNumeric int32    // 0 - 4294967295
var iniNumeric int64    // 0 - 18446744073709551615
var iniNumeric int

var iniNumeric uint8     // -128 - 127
var iniNumeric uint16    // -32768 - 32767
var iniNumeric uint32    // -2147483648 - 2147483647
var iniNumeric uint64    // -9223372036854775808 - 9223372036854775807
var iniNumeric uint

var iniNumeric float32
var iniNumeric float64

var iniNumeric rune      // 0 - 4294967295
var iniNumeric byte      // -128 - 127
```

**String**

```go
var iniString string = "Type Data String"
var iniString string = `Type Data String`
```

**Boolean**

```go
var iniBool bool = true
```

### Conditional

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

* [An Example of Using NSQ From Go](http://tleyden.github.io/blog/2014/11/12/an-example-of-using-nsq-from-go/)
* [BogoToBogo](https://www.bogotobogo.com/GoLang/GoLang_HelloWorld.php)
* [Dasar Pemrograman Golang](https://dasarpemrogramangolang.novalagung.com/)
* [Getting Started with Serverless Go](https://dev.to/yos/getting-started-with-serverless-go--1lff)
* [Golang Programs](https://www.golangprograms.com)
* [Lambdas with GoLang — a technical guide](https://cloudnative.ly/lambdas-with-golang-a-technical-guide-6f381284897b)
* [Membangun Realtime Canvas Drawing Dengan Go, Websocket dan P5.js](https://medium.com/@wuriyantomusobar/membangun-realtime-canvas-drawing-dengan-go-websocket-dan-p5-js-672c799d3044)
* [Tutorial Edge](https://tutorialedge.net/course/golang/)
* [Writing Great Go Code](https://scene-si.org/2018/07/24/writing-great-go-code/)

#### Architecture

* [Clean Architecture using Golang](https://dev.to/eminetto/clean-architecture-using-golang-5791) by [Elton Minetto](https://github.com/eminetto)
* [The Clean Code Blog](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) by [Robert C. Martin \( Uncle Bob \)](https://github.com/unclebob)
* [Trying Clean Architecture on Golang](https://hackernoon.com/golang-clean-archithecture-efd6d7c43047) by [Iman Tumorang](https://github.com/bxcodec)

#### Stackoverflow

* [Assigning null to JSON fields instead of empty strings](https://stackoverflow.com/questions/31048557/assigning-null-to-json-fields-instead-of-empty-strings)
* [gometalinter / errcheck returns a warning on deferring a func which returns a variable](https://stackoverflow.com/questions/40397781/gometalinter-errcheck-returns-a-warning-on-deferring-a-func-which-returns-a-va)

#### Docs

* [Golang](https://golang.org/doc/)

