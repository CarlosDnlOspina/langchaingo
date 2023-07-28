# 🦜️🔗 LangChain Go

[![go.dev reference](https://img.shields.io/badge/go.dev-reference-007d9c?logo=go&logoColor=white&style=flat-square)](https://pkg.go.dev/github.com/tmc/langchaingo)
[![scorecard](https://goreportcard.com/badge/github.com/tmc/langchaingo)](https://goreportcard.com/report/github.com/tmc/langchaingo)

⚡ Building applications with LLMs through composability ⚡

## 🤔 What is this?

This is the Go language implementation of LangChain.

## Unlocking Language Model Potential: Why Implementing LangChain in Go(lang) is a Strategic Choice 🚀🤖

🚀 Implementing LangChain in Go instead of Python offers several advantages that cater to the specific needs and requirements of developers. LangChain, being a framework for developing applications powered by language models, aims to go beyond simple API calls and unlock the full potential of language models by making applications data-aware and agentic. Let's explore why implementing LangChain in Go is a strategic choice:

💨 Performance and Efficiency: Go is known for its excellent performance and efficiency. Its compiled nature allows Go programs to run faster compared to interpreted languages like Python. When working with large-scale language models and processing extensive datasets, Go's speed can significantly enhance application performance and responsiveness.

🔗 Concurrency: Go's built-in concurrency features, such as goroutines and channels, enable developers to efficiently handle concurrent tasks and process multiple requests concurrently. This is especially advantageous when dealing with real-time language processing tasks or serving numerous users simultaneously.

📈 Scalability: The concurrent and efficient nature of Go makes it well-suited for building scalable applications. Language models, particularly large ones, can be resource-intensive, and Go's scalability ensures that applications can handle growing workloads without sacrificing performance.

🌐 Native API Integrations: Go has excellent support for building API servers and working with HTTP requests natively. This makes it straightforward to connect language models to various data sources, allowing the application to be data-aware, as envisioned by LangChain.

💻 System-level Programming: Go is designed for system-level programming and has a low memory footprint. This makes it ideal for developing robust language processing applications that require memory efficiency and stable performance over extended periods.

🔍 Strong Typing: Go's static typing system provides better code readability, early error detection, and enhanced maintainability. When working with complex language models and data interactions, strong typing can help catch potential issues during development, leading to more reliable applications.

👪 Ecosystem and Community: Go has a growing ecosystem and an active community of developers. By implementing LangChain in Go, developers can tap into a wealth of libraries and tools to streamline development and take advantage of community support.

🌐 Cross-platform Support: Go provides excellent cross-platform support, making it easier to deploy and run applications on various operating systems without major modifications.

## 📖 Documentation

- [API Reference](https://pkg.go.dev/github.com/tmc/langchaingo)

## 🎉 Examples

See [./examples](./examples) for example usage.

```go
package main

import (
	"context"
	"log"

	"github.com/tmc/langchaingo/llms/openai"
)

func main() {
	llm, err := openai.New()
	if err != nil {
		log.Fatal(err)
	}
	prompt := "What would be a good company name for a company that makes colorful socks?"
	completion, err := llm.Call(context.Background(), prompt)
	if err != nil {
		log.Fatal(err)
	}
	log.Println(completion)
}
```

```shell
$ go run .

Socktastic!
```
