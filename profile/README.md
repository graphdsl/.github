 # GraphDSL                                                                                                                                                                                                                                                                                                       
                                                                                                                                                                                                                                                                                                                   
  **Type-safe GraphQL Kotlin DSL code generator**                                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                                                                                   
  GraphDSL reads your GraphQL schema and generates a type-safe Kotlin DSL so you can build queries and mutations programmatically — no string templates, no typos, no guessing field names.                                                                                                                        
                                                                                                                                                                                                                                                                                                                   
  ```kotlin                                                                                                                                                                                                                                                                                                      
  val query = query("GetPost") {
      post(id = "42") {
          id
          title
          author {
              name
              email
          }
      }
  }
  // → query GetPost { post(id: "42") { id title author { name email } } }

  ---
  Projects

  ┌────────────────────────────────────────────────┬──────────────────────────────────────┐
  │                   Repository                   │             Description              │
  ├────────────────────────────────────────────────┼──────────────────────────────────────┤
  │ https://github.com/graphdsl/graphql-kotlin-dsl │ Core library, Gradle plugin, and CLI │
  ├────────────────────────────────────────────────┼──────────────────────────────────────┤
  │ https://github.com/graphdsl/graphdsl.github.io │ Documentation site                   │
  └────────────────────────────────────────────────┴──────────────────────────────────────┘

  ---
  Built with

  Language & Runtime
  - https://kotlinlang.org/ 1.9 — JVM target 17
  - https://www.graphql-java.com/ — GraphQL schema parsing
  - https://github.com/JetBrains/kotlin/tree/master/libraries/kotlinx-metadata/jvm — Kotlin type metadata inspection

  Code Generation
  - https://www.stringtemplate.org/ (ANTLR ST4) — template-driven source file generation
  - https://www.javassist.org/ — bytecode utilities

  Tooling
  - https://gradle.org/ — build system with convention plugins and included builds
  - https://ajalt.github.io/clikt/ — Kotlin CLI framework
  - https://junit.org/junit5/ — testing

  ---
  Links

  - https://graphdsl.github.io
  - https://graphdsl.github.io/getting-started
  - https://graphdsl.github.io/api/gradle-plugin
  - https://kristileka.dev
