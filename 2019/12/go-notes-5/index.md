# Go Notes 5


<!--more-->

## <font color=#cc3300>进制数，零开头的数字会被识别为8进制</font>

示例

```go
package main

import (
	"fmt"
)

func main() {
	de := 010
	fmt.Println(de)

}
```

结果是 8    虽然十个小知识点，有时候还是会记不住。