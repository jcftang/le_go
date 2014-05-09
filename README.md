logentries
=============

Golang library for logentries.com


Usage
-----
Add a new manual TCP token log at logentries.com and copy the token


```go
import (
	"github.com/bsphere/logentries"
)

func main() {
	le := logentries.LE{
		Token: "XXXX-XXXXXXXXXX-XXXXXXx-XXXXXXX",
	}

	err = le.Init()
	if err != nil {
		panic(err)
	}

	defer le.Close()

	le.Println("another test message")
}
```