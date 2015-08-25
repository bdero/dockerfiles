# devkitARM-3ds

Everything needed to build GBA, NDS, and 3DS games.

## Usage

```sh
$ docker run --rm -it -v $(pwd):/source bdero/devkitarm-3ds
```

### Examples

devkitPro is installed in `/opt/devkitPro`, with examples for the GBA and the NDS in the `examples` directory under that. Each contains several folders to demonstrate how to use various capabilities of the systems. To build an example, `cd` into its directory and run `make`. This should result in a `.gba` or `.nds` file being built, which can be run in emulators or put on flash carts.

3DS examples can be found in `/opt/devkitPro/ctrulib/libctru/examples`.

### Credits

Both the devkitARM-3ds Dockerfile as well as the readme above are from [cromo's dockerfile repo](https://github.com/cromo/dockerfiles/tree/master/devkitARM-3ds). At the time of writing this, the last build of the [original container](https://hub.docker.com/r/cromo/devkitarm-3ds/) on Docker Hub was in March 2015, but certain libraries (such as [sf2d](https://github.com/xerpi/sf2dlib/tree/master/libsf2d)), require a later version of [ctrulib](https://github.com/smealum/ctrulib) than that which was available.
