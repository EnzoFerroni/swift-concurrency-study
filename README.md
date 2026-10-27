# Swift Concurrency Study

[![iOS](https://img.shields.io/badge/iOS-26%2B-000000?logo=apple)](https://developer.apple.com/ios/)
[![Swift](https://img.shields.io/badge/Swift-Concurrency-F05138?logo=swift&logoColor=white)](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/concurrency/)
[![SwiftUI](https://img.shields.io/badge/SwiftUI-0A84FF?logo=swift&logoColor=white)](https://developer.apple.com/xcode/swiftui/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

Two small SwiftUI apps that teach `Task`, `async`/`await` and actors in Swift, made for an introductory study session at the Apple Developer Academy.

## Table of Contents

- [About](#about)
- [Examples](#examples)
- [Getting Started](#getting-started)
- [Team](#team)
- [License](#license)

## About

A didactic repository from the Apple Developer Academy | Mackenzie (2026). Each
example is a minimal app that makes one concurrency idea visible on screen, so it can
be run and discussed in a short session. The UI text and code comments are in
Portuguese.

## Examples

**Class vs Actor** (`ClasseVsActor/`)

Two counters are incremented 100,000 times from a `Task`: one stored in a regular
`class`, the other in an `actor`. The class updates instantly, while every call to the
actor is queued and awaited, which shows the cost and the safety of actor isolation
side by side.

**Actors in practice** (`ExemplosActors/`)

- `Counter`: an actor that protects a shared value from concurrent increments.
- `DataFetcher`: an actor that simulates a 2-second network call with `Task.sleep` and
  caches results by key, so repeated requests return immediately.

## Getting Started

Requirements: Xcode 26 or later.

```bash
git clone https://github.com/EnzoFerroni/swift-concurrency-study.git
cd swift-concurrency-study
open ClasseVsActor/actortest.xcodeproj    # or ExemplosActors/Exemplo.xcodeproj
```

Run on any iOS simulator. The `ExemplosActors` results are printed to the Xcode console.

## Team

<div align="center">
  <table>
    <tr>
      <td align="center" width="33%">
        <a href="https://github.com/EnzoFerroni"><img src="https://github.com/EnzoFerroni.png" width="90" alt="Enzo Ferroni"/></a>
        <br/><sub><b>Enzo Ferroni</b></sub><br/><br/>
        <a href="https://github.com/EnzoFerroni"><img src="https://skillicons.dev/icons?i=github" alt="GitHub"/></a>
        <a href="https://www.linkedin.com/in/enzoferroni/"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn"/></a>
      </td>
      <td align="center" width="33%">
        <a href="https://github.com/LuccaPV"><img src="https://github.com/LuccaPV.png" width="90" alt="Lucca Pivoto"/></a>
        <br/><sub><b>Lucca Pivoto</b></sub><br/><br/>
        <a href="https://github.com/LuccaPV"><img src="https://skillicons.dev/icons?i=github" alt="GitHub"/></a>
        <a href="https://www.linkedin.com/in/luccapivoto/"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn"/></a>
      </td>
      <td align="center" width="33%">
        <a href="https://github.com/ThomasPGR"><img src="https://github.com/ThomasPGR.png" width="90" alt="Thomas Pinheiro Grandin"/></a>
        <br/><sub><b>Thomas Pinheiro Grandin</b></sub><br/><br/>
        <a href="https://github.com/ThomasPGR"><img src="https://skillicons.dev/icons?i=github" alt="GitHub"/></a>
        <a href="https://www.linkedin.com/in/thomas-pinheiro-grandin-704bb6297/"><img src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn"/></a>
      </td>
    </tr>
  </table>
</div>

Fork of the team repository [LuccaPV/Concorrencia-Tasks-Actors](https://github.com/LuccaPV/Concorrencia-Tasks-Actors).

## License

Released under the [MIT License](LICENSE). Copyright (c) 2026 Enzo Ferroni, Lucca Pivoto
and Thomas Pinheiro Grandin.
