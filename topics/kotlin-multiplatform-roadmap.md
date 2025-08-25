# Kotlin Multiplatform roadmap

The Kotlin Multiplatform roadmap is meant as an overview of priorities and general direction for the Kotlin Multiplatform project.

The latest [roadmap blog post](https://blog.jetbrains.com/kotlin/2024/10/kotlin-multiplatform-development-roadmap-for-2025/)
was published on October 28, 2024.
The page below summarizes it and is updated whenever we reach a declared milestone or need to reflect changes in strategy:

* On February 14th, 2025, the roadmap was updated to reflect the changes described in the [Kotlin Multiplatform Tooling – Shifting Gears](https://blog.jetbrains.com/kotlin/2025/02/kotlin-multiplatform-tooling-shifting-gears/)
    blog post.

Kotlin Multiplatform goals are closely aligned with the [Kotlin roadmap](https://kotlinlang.org/docs/roadmap.html).
Be sure to check it out to have more context for the direction we're taking.

## Key priorities

* ✅ **Stable Compose Multiplatform for iOS**: We have successfully driven the iOS target to a stable release, improving the underlying framework
    and iOS-specific integrations and benchmarks.
* Better support for multiplatform development in IntelliJ-based IDEs,
    providing an optimized environment for Kotlin Multiplatform and Compose Multiplatform.
* Release the first public version of Kotlin-to-Swift export. With the initial release, we aim to provide experience comparable
    to the existing Objective-C export, and pave the way to fully leverage Swift export in the future.
* Improve the experience of creating multiplatform libraries by providing better tools and guidance. We shall improve
    the klib format to be more flexible and powerful, and provide better templates and instructions for creating multiplatform
    libraries.
* Make Amper suitable for multiplatform mobile development. In 2025, Amper should fully support multiplatform development
    for iOS and Android, including sharing UI code using Compose Multiplatform.

You can find frequently asked questions and answers in the [FAQ section](#faq).

## Recent achievements (2024-2025)

The last six months have been huge for Kotlin! Here are the major milestones we've achieved:

* ✅ **Kotlin Language Server Protocol is now in Preview** - Enhancing IDE support and development experience
* ✅ **Compose Multiplatform for iOS is now Stable** - Production-ready multiplatform UI development for iOS
* ✅ **New Kotlin Multiplatform plugin for IntelliJ IDEA and Android Studio** - Improved tooling and project setup experience
* ✅ **Kotlin Rich Errors feature is in development** - Better error reporting and debugging capabilities
* ✅ **Kotlin 'Unused return value checker' will be available in Kotlin 2.3** - Enhanced static analysis for code quality
* ✅ **Kotlin Notebook is now bundled in IntelliJ IDEA** - Interactive development and data exploration capabilities
* ✅ **Junie, the AI coding agent by JetBrains, is now available for Android Studio** - AI-powered development assistance

For the latest updates and detailed roadmap information, visit [kotl.in/roadmap](https://kotlinlang.org/docs/roadmap.html).

## Compose Multiplatform

Focus areas for Compose Multiplatform are:

* **Jetpack Compose feature parity**. Ensure that all core APIs and components are multiplatform.
* **iOS rendering performance**. Implement benchmarking infrastructure to catch regressions and make performance
    of the framework transparent to the users.
* **Feature completeness for core components**. Complete essential features, including:
    * navigation,
    * resource management,
    * accessibility,
    * internationalization.
* **General stabilization of the framework**. Improve overall stability (including interoperability between Compose and native views)
    while enhancing the user experience through Compose Multiplatform previews.
* **Documentation**. Provide users with all the resources needed to learn and use Compose Multiplatform in a single place.
* **Compose Multiplatform for web**. Reach feature parity with other supported platforms.

### Any plans regarding Compose HTML?

While continuing to maintain the Compose HTML library by fixing bugs, we are also exploring use cases for it among existing users
so that we can formulate plans for its future development.

## Tooling

We aim to ensure that Kotlin Multiplatform integrates seamlessly with the IDEs already commonly used for KMP development,
such as IntelliJ IDEA and Android Studio, making it more straightforward to share code within or between projects.

**Recent achievements:**
* ✅ **New Kotlin Multiplatform plugin for IntelliJ IDEA and Android Studio** - We've released an improved plugin that enhances the development experience with better project setup, navigation, and debugging capabilities.

We are also exploring new areas to enhance the development experience:

* Investigating building iOS apps using cloud machines to help developers who don't have convenient access to Apple devices.
* Experimenting with deeper AI tools integration to assist not only in code generation but also in more complex development tasks.

## Kotlin-to-Swift export

Our goal for 2025 is to release the first public version of direct Kotlin-to-Swift export.
The initial release aims to provide a user experience comparable to the existing Objective-C export,
while overcoming the constraints of Objective-C.

This will enable broader support for Swift language and facilitate exporting APIs,
paving the way for future improvements to fully leverage Swift export.

## Library ecosystem

As the Kotlin Multiplatform ecosystem rapidly expands, ensuring the backward compatibility of libraries becomes crucial.
Here's what we plan to do:

* Improve the klib format to allow library creators to leverage their knowledge of building JVM libraries.
* Implement the same code-inlining behavior in Kotlin Multiplatform libraries as for the JVM.
* Provide a tool that ensures your multiplatform library public API remains backward compatible.

We’re also looking to improve the publishing process for Kotlin Multiplatform libraries. We want to:

* Provide templates and comprehensive guidelines for creating and publishing KMP libraries.
* Stabilize klib cross-compilation on different platforms.
* Launch a fully re-designed KMP library publication process.
* Significantly improve the libraries' documentation process.

While Kotlin Multiplatform will receive significant updates, libraries build with the current format will still work
with newer Kotlin versions.

### Improving search for multiplatform libraries

There are now more than 2500 Kotlin Multiplatform libraries available.
However, despite the extensive selection, it can be challenging for developers to find libraries that meet their specific
needs and support their chosen platforms.

Our goal is to introduce a solution that facilitates the discovery of these libraries and allows developers to try them out easily.

### Amper

Amper is an experimental project configuration and build tool by JetBrains. In 2025, we will focus on making Amper fully
suitable for multiplatform mobile app development for Android and iOS, with shared Compose Multiplatform UI.

We aim to support:

* Running and testing applications locally, on physical devices, and within CI.
* Signing applications and publishing them in the Play Store and App Store.
* IDE integration to ensure a smooth and enjoyable experience.

### Gradle and other build tools

As we look ahead to 2025, our work on Gradle enhancements is outlined in the [Kotlin roadmap](https://kotlinlang.org/docs/roadmap.html#tooling).

Here are the key areas we will be working on regarding Kotlin Multiplatform in particular:

* Support declaring Kotlin Multiplatform dependencies at the project level. This will make it easier for developers
    to manage their project dependencies effectively.
* Improve integration of the Kotlin/Native toolchain into Gradle.
* Implement the next-generation distribution format for multiplatform libraries.
    This will simplify the dependencies model and publication layout for multiplatform libraries, making them easier
    to use with third-party build tools and reducing complexity for library authors.
* Provide full support for Kotlin Multiplatform in Declarative Gradle.
    Our work on the Experimental Kotlin Ecosystem Plugin, which supports Declarative Gradle, aims to help developers
    explore a declarative approach to their Gradle builds.

> * This roadmap is not an exhaustive list of all things the team is working on, only the biggest projects.
> * There's no commitment to delivering specific features or fixes in specific versions.
> * We will adjust our priorities as we go and update the roadmap accordingly.
>
{style="note"}

## FAQ

### Can you fix KMP support in IntelliJ IDEA?

We recognize the importance of providing a great KMP experience in IntelliJ IDEA.
As stated in the [blog post about KMP tooling](https://blog.jetbrains.com/kotlin/2025/02/kotlin-multiplatform-tooling-shifting-gears/),
we will be focusing exclusively on enhancing KMP support for the IntelliJ Platform as a whole.
This will include improving quality and stability and introducing certain features so that developers who prefer
IntelliJ IDEA for multiplatform development can enjoy full KMP support in their preferred IDE.

### What about KMP support in Android Studio?

We are actively collaborating with Google to improve KMP support in Android Studio.
More detailed plans will be available at a later date.
Stay tuned!

### What is the recommended IDE for KMP development now?

If your primary use case is mobile, we recommend using Android Studio.
We're also working on providing great support in IntelliJ IDEA.

### Will Swift be available in IntelliJ IDEA and Android Studio?

Swift is an important part of certain KMP scenarios, and we are working on supporting these use cases.

### Are you giving up on the web?

No, we're not giving up on the web at all!
We're actively working on Kotlin/Wasm support as well as on Compose Multiplatform for web to achieve feature parity
with other platforms.
Our current efforts include implementing drag-and-drop support, improving text input and rendering, and ensuring seamless
interoperability with HTML content.
We will share more detailed plans for the web soon. Stay tuned!

### What about Compose HTML?

While continuing to maintain the Compose HTML library by fixing bugs, we are also exploring use cases for it among existing users
so that we can formulate plans for its future development.