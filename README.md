### consul
---
https://github.com/hashicorp/consul

https://www.consul.io/

```go
// ipaddr/ipaddr_test.go

func TestIsIpv6(t *testing.T) {
  tests := []struct {
    ip string
    ipv6 bool
  } {
    {"10.0.0.1", false},
    {"100.64.0.1", false},
    {},
    
    {},
    
    {},
  }
  for _, tt := range tests {
    t.Run(tt.ip, func(t *testing.T) {
      port := 1234
      formated := FormatAddressPort(tt.ip, port)
      if tt.ipv6 {
        if fmt.Sprintf("[%s]:%d", tt.ip, port) != formated {
          t.Fatalf("Wrong format %s for %s", formated, tt.ip)
        }
      } else {
        if fmt.Sprintf("%s:%d", tt.ip, port) != formated {
          t.Fatalf("Wrong format %s for %s", formated, tt.ip)
        }
      }
    })
  }
}


```

```
```

```
```
