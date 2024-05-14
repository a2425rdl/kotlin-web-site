[//]: # (title: Compatibility guide for Kotlin 2.0)

_[Keeping the Language Modern](kotlin-evolution.md)_ and _[Comfortable Updates](kotlin-evolution.md)_ are among the fundamental principles in
Kotlin Language Design. The former says that constructs which obstruct language evolution should be removed, and the
latter says that this removal should be well-communicated beforehand to make code migration as smooth as possible.

As we introduce the Kotlin K2 compiler as part of Kotlin 2.0, this compatibility guide is focused on changes that are
**NOT** related to the compiler. For details on compatibility with the new K2 compiler, see [K2 compiler migration guide](k2-compiler-migration-guide.md).

While most of the language changes were already announced through other channels, like updated changelogs or compiler
warnings, this document and the [K2 compiler migration guide](k2-compiler-migration-guide.md), provide a complete reference for migration from Kotlin 1.9 to Kotlin 2.0.

## Basic terms

In this document we introduce several kinds of compatibility:

- _source_: source-incompatible change stops code that used to compile fine (without errors or warnings) from compiling
  anymore
- _binary_: two binary artifacts are said to be binary-compatible if interchanging them doesn't lead to loading or
  linkage errors
- _behavioral_: a change is said to be behavioral-incompatible if the same program demonstrates different behavior
  before and after applying the change

Remember that those definitions are given only for pure Kotlin. Compatibility of Kotlin code from the other languages
perspective
(for example, from Java) is out of the scope of this document.

## Language

<!--
### Title

> **Issue**: [KT-NNNNN](https://youtrack.jetbrains.com/issue/KT-NNNNN)
>
> **Component**: Core language
>
> **Incompatible change type**: source
>
> **Short summary**:
>
> **Deprecation cycle**:
>
> - 1.6.20: report a warning
> - 1.8.0: raise the warning to an error
-->

## Tools

### Visibility changes in Gradle

> **Issue**: [KT-67227](https://youtrack.jetbrains.com/issue/KT-67227)
>
> **Component**: Gradle
>
> **Incompatible change type**: source
>
> **Short summary**:
>
> **Deprecation cycle**:
>
> - 1.6.20: report a warning
> - 1.8.0: raise the warning to an error

### Deprecate old compiler option DSLs

> **Issue**: [KT-67234](https://youtrack.jetbrains.com/issue/KT-67234)
>
> **Component**: Gradle
>
> **Incompatible change type**: source
>
> **Short summary**: The ability to configure the `compilerOptions` property in the `kotlinCompilation` DSL has been deprecated. 
> The `kotlinOptions` DSL has also been deprecated.
>
> **Deprecation cycle**:
>
> - 2.0.0: report a warning

### Gradle dependency handling of CInteropProcess

> **Issue**: [KT-67226](https://youtrack.jetbrains.com/issue/KT-67226)
>
> **Component**: Gradle
>
> **Incompatible change type**: source
>
> **Short summary**:
>
> **Deprecation cycle**:
>
> - 1.6.20: report a warning
> - 1.8.0: raise the warning to an error

### Remove kotlin.useK2 Gradle property

> **Issue**: [KT-67430](https://youtrack.jetbrains.com/issue/KT-67430)
>
> **Component**: Gradle
>
> **Incompatible change type**: source
>
> **Short summary**: The `kotlin.useK2` Gradle property has been removed.
>
> **Deprecation cycle**:
>
> - 1.8.20: the `kotlin.useK2` Gradle property is deprecated
> - 2.0.0: the `kotlin.useK2` Gradle property is removed

### Remove deprecated platform plugin IDs

> **Issue**: [KT-67431](https://youtrack.jetbrains.com/issue/KT-67431)
>
> **Component**: Gradle
>
> **Incompatible change type**: source
>
> **Short summary**: support for these platform plugin IDs have been removed:
> * `kotlin-platform-android`
> * `kotlin-platform-jvm`
> * `kotlin-platform-js`
> * `org.jetbrains.kotlin.platform.android`
> * `org.jetbrains.kotlin.platform.jvm`
> * `org.jetbrains.kotlin.platform.js`
>
> **Deprecation cycle**:
>
> - 1.3: the platform plugin IDs are deprecated
> - 2.0.0: the platform plugin IDs are no longer supported