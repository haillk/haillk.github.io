# 复制变量恢复至锁状态


<!--more-->

### ## 已经加锁的变量复制后，会将锁的状态一起复制

例子：

```go
 1type MyMutex struct {
 2    count int
 3    sync.Mutex
 4}
 5
 6func main() {
 7    var mu MyMutex
 8    mu.Lock()
 9    var mu1 = mu
10    mu.count++
11    mu.Unlock()
12    mu1.Lock()
13    mu1.count++
14    mu1.Unlock()
15    fmt.Println(mu.count, mu1.count)
16}
```

例子中，mu1将mu的锁状态一起复制了，所以不能再次加锁。最终会fatal error