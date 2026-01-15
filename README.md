# gomobile with tvOS Support

This is a fork of the official [golang.org/x/mobile](https://go.googlesource.com/mobile) repository that adds support for Apple tvOS targets.

## What's Different

This fork extends gomobile to support building Go libraries for tvOS and tvOS Simulator, in addition to the standard iOS, iOS Simulator, macOS, Mac Catalyst, and Android targets.

### Added Targets

- `tvos` - Apple tvOS (arm64)
- `tvossimulator` - Apple tvOS Simulator (arm64, amd64)

### New Build Flag

- `-tvosversion` - Minimum tvOS version (default: 13.0)

## Usage

### Building for tvOS

```bash
gomobile-netbird bind -target=tvos ./package
```

### Building for tvOS Simulator

```bash
gomobile-netbird bind -target=tvossimulator ./package
```

### Building an XCFramework with tvOS Support

```bash
gomobile-netbird bind -target=ios,iossimulator,tvos,tvossimulator -o MyFramework.xcframework ./package
```

## Installation

```bash
go install github.com/netbirdio/gomobile-tvos-fork/cmd/gomobile-netbird@latest
go install github.com/netbirdio/gomobile-tvos-fork/cmd/gobind-netbird@latest
```

## Original Project

This fork is based on the Go Mobile project from [golang.org/x/mobile](https://pkg.go.dev/golang.org/x/mobile). The original project provides:

- [Building all-Go apps](https://golang.org/x/mobile/app)
- [Building libraries for SDK apps](https://golang.org/x/mobile/cmd/gobind)

For general gomobile documentation and usage, see [golang.org/wiki/Mobile](https://golang.org/wiki/Mobile).

## License

This project retains the original BSD-style license from the Go project. See the [LICENSE](LICENSE) file for details.
