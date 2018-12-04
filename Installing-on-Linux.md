### Installation

First, install the keylogger:

`pip install keylogger`

and there are several options that can be set with environment variables:

* `--log-file output.og`: File path to use as the log file.  Default is current directory.
* `--cancel-key`: The key that uses as the cancel key, default is '`'.
* `--clean-log`: clean the log file first, default is No.

### How to run it?

To run it just type `keylogger` and it'll run:
```
keylogger --log-file keylogger.log 
RECORD extension version 1.13
```

The keylogger is now running! It will log your strokes to the file you
specified. Stop it by hitting the cancel key (grave or \`, if not set with
`--cancel-key`. That's the one under escape on a standard keyboard.)

You can make it run on startup:

`$ sudo make startup`