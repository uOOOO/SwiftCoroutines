### Swift/Coroutines interop

This is the code associated with [this blog post](https://dev.to/touchlab/working-with-kotlin-coroutines-and-rxswift-24fa). 

The `shared` directory contains Kotlin code, including a `ThingRepository` in common and a wrapper `ThingRespositoryIos` in the ios sources, which makes use of interop utilities in `SwiftCoroutines.kt`. 

The Kotlin code is consumed by an Xcode project in the `ios` directory. In there, `RxSwiftWrappers.swift` defines the RxSwift linkages to the coroutine wrappers in `SwiftCoroutines.kt`, and makes a demo call in `ViewController.swift`. There are also unit tests in `SwiftCoroutinesTests.swift` which, while not exhaustive, verify most of the workings of the interop code, including checking multithreaded usage.
