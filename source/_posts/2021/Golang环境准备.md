layout: "post"
title: "Golang环境准备"
date: "2021-02-14 17:38"
---
# GOPATH作用
1. The Go path is used to resolve import statements
2. When using modules, GOPATH is no longer used for resolving imports. However, it is still used to store downloaded source code (in GOPATH/pkg/mod) and compiled commands (in GOPATH/bin)
