# {{raw-name}}

{{description}}

## Usage

### Building the Uberjar

1. `make clean && make build`

### Running the MCP server
Some example commands you can try in Claude Desktop or Inspector:

1. Visualize this data for me using ...
2. Add the prompts you would use to test your server in this section

#### Before running the MCP server
Remember:
1. Replace the full-path to the `{{name}}` JAR with the correct path on your system (i.e. replace `/Users/vedang/repo-name` below with the correct path)
2. Other notes specific to your server should go here.

#### In Claude Desktop

```json
    "{{main/file}}": {
      "command": "java",
      "args": [
        "-Dclojure.tools.logging.factory=clojure.tools.logging.impl/log4j2-factory",
        "-Dorg.eclipse.jetty.util.log.class=org.eclipse.jetty.util.log.Slf4jLog",
        "-Dlog4j2.contextSelector=org.apache.logging.log4j.core.async.AsyncLoggerContextSelector",
        "-Dlog4j2.configurationFile=log4j2-mcp.xml",
        "-Dbabashka.json.provider=metosin/jsonista",
        "-Dlogging.level=INFO",
        "-cp",
        "/Users/vedang/repo-name/target/{{name}}-1.0.0.jar",
        "{{top/ns}}.{{main/ns}}"
      ]
    }
```

#### In MCP Inspector
Remember to use the full-path to the `{{name}}` JAR on your system.

```shell
npx @modelcontextprotocol/inspector java -Dclojure.tools.logging.factory=clojure.tools.logging.impl/log4j2-factory -Dorg.eclipse.jetty.util.log.class=org.eclipse.jetty.util.log.Slf4jLog -Dlog4j2.contextSelector=org.apache.logging.log4j.core.async.AsyncLoggerContextSelector -Dlog4j2.configurationFile=log4j2-mcp.xml -Dbabashka.json.provider=metosin/jsonista -Dlogging.level=INFO -cp /Users/vedang/repo-name/target/{{name}}-1.0.0.jar {{top/ns}}.{{main/ns}}
```

## License

Copyright © {{now/year}} {{developer}}

Distributed under the MIT License
