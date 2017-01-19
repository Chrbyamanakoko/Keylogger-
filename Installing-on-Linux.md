### Installation
You'll need to install python-xlib if you don't have it.

You can install it using `pip`:

`pip install python-xlib`

...or your system package manager:

`sudo apt-get install python-xlib`

Check that you have git installed, and then run this.

`git clone https://github.com/GiacomoLaw/Keylogger`

This will clone this entire repo. Find the linux folder, extract it, and open it. Rename the extracted folder to `linux-logger` Then run this:

`giacomo@vostro:~$ cd linux-logger/`

### Options
There are several options that can be set with environment variables:

- `pylogger_file`: File path to use as the log file.
Default: `~/Desktop/file.log`
- `pylogger_cancel`: The key to use as the cancel key, in character form.
Default: \`
- `pylogger_clean`: Whether to clear the file on startup. This can be set to anything to clear the file.
Default: No (not set)

### Running

You can use Python 2 or 3 to run the logger.

To run it:
```
$ python keylogger.py
<class 'Xlib.protocol.request.QueryExtension'>
<class 'Xlib.protocol.request.QueryExtension'>
RECORD extension version 1.13
```

Or, using the options mentioned above:
```bash
# This tells the logger to use /home/me/myfile.txt,
# clearing the file on startup, and using ! as the
# cancel key.
# You don't have to use all of these options at once, or any at all.
$ pylogger_file="/home/me/myfile.txt" pylogger_clean=1 pylogger_cancel="!" python keylogger.py
```

The keylogger is now running! It will log your strokes to the file you
specified. Stop it by hitting the cancel key (grave or \`, if not set with
`pylogger_cancel`. That's the one under escape on a standard keyboard.)

You can make it run on startup:

`$ sudo make startup`