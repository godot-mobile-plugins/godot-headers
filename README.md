# godot-headers

Pre-built static and generated header files from iOS builds of the [Godot game engine](https://godotengine.org), published automatically for every Godot release.

## What's in each release

Each release corresponds to a tag from [godotengine/godot-builds](https://github.com/godotengine/godot-builds) and follows the same naming convention - `<version>-<flavor>`, for example `4.6.2-rc2` or `4.5.2-stable`.

The attached archive contains every `*.glsl`, `*.h`, `*.hh`, `*.hpp`, `*.inc`, and `*.inl` file produced by an iOS `template_debug` SCons build of that Godot version. These headers are useful for native iOS plugins that need to compile against Godot's internal API without building the engine from source themselves.

## Using the headers

1. Go to the [Releases](https://github.com/godot-mobile-plugins/godot-headers/releases) page and download the archive for the Godot version you are targeting.
2. Extract the archive and add the header paths to your Xcode project or build system's include search paths.
3. Link against your own Godot export template as usual.

## Release schedule

New releases are checked for and created automatically twice a week - every **Wednesday** and **Sunday** at 03:00 UTC - via the [Archive Godot Headers](.github/workflows/archive-godot-headers.yml) workflow. The workflow compares the 10 most recent releases in `godotengine/godot-builds` against this repository and builds any that are missing.

A release can also be triggered manually for a specific version from the [Actions](https://github.com/godot-mobile-plugins/godot-headers/actions) tab.

## Related

- [godotengine/godot](https://github.com/godotengine/godot) - Godot engine source
- [godotengine/godot-builds](https://github.com/godotengine/godot-builds) - official Godot release tags
- [ActionCommons/build-godot](https://github.com/ActionCommons/build-godot) - the GitHub Action used to produce these archives
