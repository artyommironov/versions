# Latest dependency versions

## Usage

In setting.gladle.kts
```kotlin
enableFeaturePreview("VERSION_CATALOGS")

dependencyResolutionManagement {
  versionCatalogs {
    create("libs") {
      from(files("versions/android.versions.toml"))
    }
  }
}

include(":app")
```

In build.gradle.kts
```
buildscript {
  dependencies {
    classpath(libs.androidPlugin)
    classpath(libs.kotlinPlugin)
    // etc
  }
}

```

In app/build.gradle.kts
```kotlin
dependencies {
  implementation(libs.androidxCoreKtx)
  // etc
}
```
