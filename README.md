## Synopsis

**sblg** is a utility for creating static blogs.  It merges articles
into templates, generating static HTML files, Atom feeds, and JSON
files.  It's built for use with `make`-style build environments.

This is a read-only repository for tracking development of the system
and managing bug reports and patches.  (Feature requests will be just be
closed, sorry!) Stable releases, documentation, and general information
are all available at the [website](https://kristaps.bsd.lv/sblg).

If you have any comments or patches, please feel free to post them here.

## Building with CMake

In 2021, a fork of the sblg project added CMake build support. The project is relatively simple, but relies on the `libexpat` dependency. The official method for installing the dependency is to use `vcpkg` (although on \*nix systems you could use the `libexpat-dev` or equivalent package).

###  Installing Dependencies

- Install [vcpkg](https://vcpkg.io/en/getting-started.html)
- Run `vcpkg install expat`

### Building sblg

```sh
cmake -B ./build -S . -DCMAKE_TOOLCHAIN_FILE=/home/matsu/vcpkg/scripts/buildsystems/vcpkg.cmake
cmake --build ./build
```

Remember, you need to match the `vcpkg` target triplet that you installed (i.e. `x64-linux`). You can also specify that on the command line: `VCPKG_TARGET_TRIPLET`.


## License

All sources use the ISC license.
See the [LICENSE.md](LICENSE.md) file for details.
