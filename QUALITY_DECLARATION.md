This document is a declaration of software quality for the `foonathan_memory` package imported by `foonathan_memory_vendor`, based on the guidelines in [REP-2004](https://www.ros.org/reps/rep-2004.html).

# `foonathan_memory` Quality Declaration

This quality declaration claims that the third party package `foonathan_memory` is in the **Quality Level 3** category.

Below are the rationales, notes, and caveats for this claim, organized by each requirement listed in the [Package Requirements for Quality Level 3 in REP-2004](https://www.ros.org/reps/rep-2004.html).

## Version Policy

### Version Scheme

`foonathan_memory` is in the beta stage, and currently has a version less than 1.0. The public API may change between minor version updates.

### API Stability Within a Released ROS Distribution

`foonathan_memory` is a third party package and does not follow the ROS distribution timeline. It may introduce breaking API changes within a ROS distribution.

### ABI Stability Within a Released ROS Distribution

`foonathan_memory` is a third party package and does not follow the ROS distribution timeline. It may introduce breaking ABI changes within a ROS distribution.

### Public API Declaration

All symbols in the installed headers are considered part of the public API with the exception of the `detail` directory and corresponding namespace.

All installed headers are in the `include` directory of the package, headers in any other folders are not installed and considered private.

## Change Control Process

`foonathan_memory` is actively maintained by one individual, many changes are committed directly by its maintainer.
Changes from external contributors are reviewed by the maintainer.


Changes must pass CI on AMD 64 for:
- Ubuntu 16.04 for gcc 4.9 and 5.5
- MacOS with XCode 9.4 with Apple LLVM version 9.1.0
- Windows with Microsoft Visual Studio 2015, MSVC 18.0

ARM 64 support is not directly evaluated by this package's CI process.

## Documentation

### Feature Documentation

`foonathan_memory` has a [feature list](https://foonathan.net/memory/index.html) with descriptions of its main features.

### Public API Documentation

`foonathan_memory` has embedded API documentation and it is generated using doxygen and is [hosted](https://foonathan.net/memory/index.html) alongside the feature documentation.
There is documentation for nearly all of the public API.

### License

The license for `foonathan_memory` is zlib, a summary statement is provided in each source file, and a full copy of the license is in the `LICENSE` file.

### Copyright Statements

The copyright holders each provide a statement of copyright in each source code file in `foonathan_memory`.

## Testing

### Feature Testing

Many features in `foonathan_memory` have corresponding tests which simulate typical usage, and they are located in the `test` directory.

### Public API Testing

Many parts of the public API have tests.

### Coverage

`foonathan_memory` does not track testing coverage.

### Performance

`foonathan_memory` does not conduct performance tests.

### Linters and Static Analysis

`foonathan_memory` does not conduct tests with linters on its public CI.

## Dependencies

`foonathan_memory` does not have any dependencies outside of the C++ standard library.

## Platform Support

`foonathan_memory` supports the following platforms and tests each one:
- Ubuntu 16.04 for gcc 4.9 and 5.5
- MacOS with XCode 9.4 with Apple LLVM version 9.1.0
- Windows with Microsoft Visual Studio 2015, MSVC 18.0

ARM 64 support is not directly evaluated by this package's CI process.
