

## 在指定-v之后，设置输出级别

```
import (
    "testing"
    "os"
)

func TestMain(m *testing.M) {
    for _, arg := range os.Args {
        if arg == "-test.v=true" {
            log.Log.SetLevel(log.DebugLevel)
            break
        }
    }
}
```
