---
published: true
title: Fibonnaci in golang 
layout: post
tags: [golang, fibonacci]
---
A tiny little function written to get nth fibonnaci number in golang.

```go

package main

import (
	"fmt"
	"time"
)

func main() {
	fmt.Println("Hello, playground")
	
	fmt.Println(Fibonnaci(1))
	fmt.Println(Fibonnaci(2))
	fmt.Println(Fibonnaci(3))
	fmt.Println(Fibonnaci(4))
	fmt.Println(Fibonnaci(5))
	fmt.Println(Fibonnaci(6))
	
	fmt.Println(Fibonnaci(7))
	fmt.Println(Fibonnaci(8))
	fmt.Println(Fibonnaci(9))
	fmt.Println(Fibonnaci(10))
	fmt.Println(Fibonnaci(11))
	fmt.Println(Fibonnaci(12))
	
	fmt.Println(Fibonnaci(13))
	fmt.Println(Fibonnaci(14))
	fmt.Println(Fibonnaci(15))
	fmt.Println(Fibonnaci(16))
	fmt.Println(Fibonnaci(17))
	fmt.Println(Fibonnaci(18))
	
	fmt.Println(Fibonnaci(19))
	fmt.Println(Fibonnaci(20))
	fmt.Println(Fibonnaci(21))
	fmt.Println(Fibonnaci(22))
	fmt.Println(Fibonnaci(23))
	
	fmt.Println(Fibonnaci(24))
	fmt.Println(Fibonnaci(240))
}

var lookup map[int]int64 = map[int]int64{}

func Fibonnaci(i int) int64 {

	val, ok := lookup[i]
	if ok {
		return val
	}
	

	if i == 1 {
		return 1
	} else if i == 2 {
		return 1
	}
	
	val = Fibonnaci(i -1) + Fibonnaci(i -2)
	lookup[i] = val
	
	return val
}
```