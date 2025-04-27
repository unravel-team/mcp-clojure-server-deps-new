# tech.unravel/mcp-clojure-server-template

A `deps-new` template to create MCP Servers quickly.

## Usage

This is a template project for use with [deps-new](https://github.com/seancorfield/deps-new).

It will produce a new MCP Server project when run:

    $ clojure -Sdeps '{:deps {tech.unravel/mcp-clojure-server-template {:git/url "https://github.com/unravel-team/mcp-clojure-server-deps-new" :git/sha "1d89718d5b1f27d071704072b21c27f8eb65a84a"}}}' -Tnew create :template tech.unravel/mcp-clojure-server-template :name mygroupid/mycoolmcpserver

Assuming you have installed `deps-new` as your `new` "tool" via:

```bash
clojure -Ttools install-latest :lib io.github.seancorfield/deps-new :as new
```

Run this template project's tests (by default, this just validates your template's `template.edn`
file -- that it is valid EDN and it satisfies the `deps-new` Spec for template files):

    $ clojure -T:build test

## License

Copyright © 2025 Unravel.tech Engineering

Distributed under the MIT License
