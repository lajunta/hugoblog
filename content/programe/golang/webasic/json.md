---
title: "Golang Test Json"
date: 2021-04-04T23:56:54+08:00
draft: false
tags: ["golang","web"]
---
JSON 
===

json 编码与解码例子

```go
// json.go
package main

import (
    "encoding/json"
    "fmt"
    "net/http"
)

type User struct {
    Firstname string `json:"firstname"`
    Lastname  string `json:"lastname"`
    Age       int    `json:"age"`
}

func main() {
    http.HandleFunc("/decode", func(w http.ResponseWriter, r *http.Request) {
        var user User
        json.NewDecoder(r.Body).Decode(&user)

        fmt.Fprintf(w, "%s %s is %d years old!", user.Firstname, user.Lastname, user.Age)
    })

    http.HandleFunc("/encode", func(w http.ResponseWriter, r *http.Request) {
        peter := User{
            Firstname: "John",
            Lastname:  "Doe",
            Age:       25,
        }

        json.NewEncoder(w).Encode(peter)
    })

    http.ListenAndServe(":8080", nil)
}
```

### curl test

```bash
$ curl -s -XPOST -d'{"firstname":"Elon","lastname":"Musk","age":48}' http://localhost:8080/decode
Elon Musk is 48 years old!

$ curl -s http://localhost:8080/encode
{"firstname":"John","lastname":"Doe","age":25}
```