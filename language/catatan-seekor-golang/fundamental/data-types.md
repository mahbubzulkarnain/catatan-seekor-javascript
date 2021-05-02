# Data Types

#### **Numeric**

```go
// Decimal default value = 0.0

var iniNumeric float32
var iniNumeric float64

// Non-Decimal default value = 0
// Note: https://www.h-schmidt.net/FloatConverter/IEEE754.html

var iniNumeric uint8     // 0 - 255
var iniNumeric uint16    // 0 - 65535
var iniNumeric uint32    // 0 - 4294967295
var iniNumeric uint64    // 0 - 18446744073709551615
var iniNumeric uint

var iniNumeric int8     // -128 - 127
var iniNumeric int16    // -32768 - 32767
var iniNumeric int32    // -2147483648 - 2147483647
var iniNumeric int64    // -9223372036854775808 - 9223372036854775807
var iniNumeric int

var iniNumeric rune      // -2147483648 - 2147483647
var iniNumeric byte      // 0 - 255

```

#### **String**

```go
// String default value = ""
var iniString string

var iniString string = "Type Data String"
var iniString string = "Type " +
    "Data " +
    "String"

var iniString string = `Type Data String`
var iniString string = `Type 
Data 
String`
```

#### **Boolean**

```go
// Bool default value = false
var iniBool bool = true
```

### 

