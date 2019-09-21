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

* [BogoToBogo](https://www.bogotobogo.com/GoLang/GoLang_HelloWorld.php)
* [Dasar Pemrograman Golang](https://dasarpemrogramangolang.novalagung.com/)
* [Getting Started with Serverless Go](https://dev.to/yos/getting-started-with-serverless-go--1lff)
* [Lambdas with GoLang — a technical guide](https://cloudnative.ly/lambdas-with-golang-a-technical-guide-6f381284897b)
* [Membangun Realtime Canvas Drawing Dengan Go, Websocket dan P5.js](https://medium.com/@wuriyantomusobar/membangun-realtime-canvas-drawing-dengan-go-websocket-dan-p5-js-672c799d3044)
* [Tutorial Edge](https://tutorialedge.net/course/golang/)

#### Docs

* [Golang](https://golang.org/doc/)

