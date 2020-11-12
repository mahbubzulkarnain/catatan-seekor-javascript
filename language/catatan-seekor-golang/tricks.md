# Tricks

```go
func GetFuncName(fn interface{}) string {
	return runtime.FuncForPC(reflect.ValueOf(fn).Pointer()).Name()
}
```

```go
func CallFuncWithParams(jobFunc interface{}, params []interface{}) ([]reflect.Value, error) {
	f := reflect.ValueOf(jobFunc)
	if len(params) != f.Type().NumIn() {
		return nil, errors.New("the number of params is not adapted")
	}

	in := make([]reflect.Value, len(params))
	for k, param := range params {
		in[k] = reflect.ValueOf(param)
	}

	return f.Call(in), nil
}

```

```go
func Currency(nominal interface{}) string {
	p := message.NewPrinter(language.Indonesian)
	return fmt.Sprintf("IDR %v", p.Sprint(nominal))
}
```

```go
func FNCheck(fn func() error) {
	if err := fn(); err != nil {
		fmt.Println(err.Error())
	}
}
```

