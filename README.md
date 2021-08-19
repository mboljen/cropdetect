# cropdetect

This bash script detects black margins of video files.  A recent version of `ffmpeg` is required.

## Installation

Use the following command to install this software:

```bash
$ make
$ make install
```

The default `PREFIX` is set to `/usr/local`.  In order to successfully complete the installation, you need to have write permissions for the installation location.

## Usage

```bash
$ cropdetect [-s skiptime] [-t scantime] [-c limit:round:skip:reset] videofile
```

`cropdetect` will skip `skiptime` seconds from the beginning and parse `scantime` seconds of the file `videofile` in order to detect potential black margins.  The expected unit is seconds.  The default of `scantime` is 5 percent of the total duration of the video.  The default of `skiptime` is 2 percent of the total duration of the video.  The `cropdetect` filter of `ffmpeg` can be specified if needed.  It defaults to `24:16:2:0`.



## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
