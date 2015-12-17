# Test Boost.Python on Android

## Build

You need to copy your prebuilt Python in the `copy/` directory
such that your `copy/` directory looks somehow like this.

    copy/
    copy/site-packages
    copy/site-packages/README
    copy/stdlib.zip
    copy/python
    copy/modules
    copy/modules/unicodedata.so
    copy/modules/_ctypes.so
    copy/modules/select.so
    copy/modules/_socket.so
    copy/modules/_sqlite3.so
    copy/modules/_multiprocessing.so
    copy/modules/pyexpat.so
    copy/main.py
    copy/libpython3.5m.so

In the directory https://dl.crystax.net/ndk/linux/current/cache/android/
there is for example `python3.5-libs-armeabi.tar.xz`
which contains exactly these files in some subdirectory.

Run make and it will `ndk-build`, `adb push` and run the `test` executable.