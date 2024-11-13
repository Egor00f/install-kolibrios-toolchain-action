# Install kolibrios toolchain action 

This is the installer of the gcc toolchain for kolibrios as github action.

It using installation scripts from https://github.com/Egor00f/kolibrios-gcc-toolchain


Example:

```
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: Egor00f/install-kolibrios-toolchain-action@main

      - name: Test toolchain working
        run: |
          /home/autobuild/tools/win32/bin/kos32-gcc -v
          /home/autobuild/tools/win32/bin/kos32-g++ -v
          /home/autobuild/tools/win32/bin/kos32-ar -V 
          /home/autobuild/tools/win32/bin/kos32-objcopy -V
          /home/autobuild/tools/win32/bin/kos32-strip -V
```
