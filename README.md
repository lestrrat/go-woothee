go-woothee
==========

[Woothee](https://github.com/woothee) is a multi-language UserAgent detection library, and this is the Go version of Woothee.

```go
import (
    "github.com/lestrrat/go-woothee"
)

func main() {
    agent := `Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)`
    result, err := woothee.Parse(agent)
    if err != nil {
        log.Fatalf("Could not parse '%s': %s", agent, err)
    }

    /*
        result.Name     = "Googlebot"
        result.Category = "crawler"
        result.Os       = "UNKNOWN"
        result.Type     = "UNKNOWN"
        result.Version  = "UNKNOWN"
        result.Vendor   = "UNKNOWN"
    */
}
```
