# Core public binaries

Consumers integrate **published** Core artifacts — not the private Bitbucket source tree.

## Coordinates

| Platform | How |
| --- | --- |
| Android | Maven Central: `ae.network:ni-card-management-sdk-core:<VERSION>` |
| iOS (SPM) | GitHub Release zip via thin `Package.swift` on [`network-international/card-management-sdk-core`](https://github.com/network-international/card-management-sdk-core) |

Replace `<VERSION>` with the Core semver you need (see Release tags / Maven versions).

### Gradle

```gradle
implementation "ae.network:ni-card-management-sdk-core:<VERSION>"
```

### Swift Package Manager

Depend on the public Core repository tag matching `<VERSION>` (binaryTarget URL points at that Release’s `NICardManagementSDKCore.xcframework.zip`).

## What is not published

- Source code (Bitbucket private)
- iOS dSYMs
- Android R8 mapping / seeds

Debug symbols for a specific Core version are available from Network International support on request.

## Integrity

Each GitHub Release includes `checksums.txt` (SHA-256). SPM also requires the zip checksum embedded in `Package.swift`.
