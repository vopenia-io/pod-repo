
### Configuration

In your Podfile, add the following at the beginning of the file:

***Podfile***

```
source "https://cdn.cocoapods.org/"
source "https://github.com/livekit/podspecs"
source "https://github.com/vopenia-io/pod-repo"
```

This will make sure you can download and install both LiveKitClient & LiveKitClientKotlin (or any other pods defined here)

***build.gradle.kts***

For Kotlin Multiplatform, in order to include the 2 pods, make the following changes :

```
kotlin {
    ...

    cocoapods {
        summary = ...
        homepage = ...
        version = ...
        specRepos {
            url("https://github.com/livekit/podspecs")
            url("https://github.com/vopenia-io/pod-repo")
        }
    }
}
```