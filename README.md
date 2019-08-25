# Tools for go

This is a catch-all repository to dump tools I've written for Go. It might or
might not continue to be filled and maintained in the future.

# redundantbranch

A `golang.org/x/tools/analysis` analyzer that finds break/continue/goto
statements that don't affect control flow. You can look into
[redundantbranch/testdata](redundantbranch/testdata) for examples of what that
means. There are sometimes reasons to have such redundancy - it can make it
easier to understand a large switch-statement and it can guard against future
modifications breaking code. So it should be treated as a lint-check and its
reports should be considered on a case-by-case basis.

You can install a standalone binary of this check using
```
go get github.com/Merovius/go-tools/cmd/redundantbranch
```

# License

```
Copyright 2019 Axel Wagner

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
