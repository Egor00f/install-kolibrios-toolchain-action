#Install kolibrios toolchain action 

This is the installer of the gcc toolchain for colibrios in the form of github action.

it using instalation script from https://github.com/Egor00f/kolibrios-gcc-toolchain


example:
```
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: egor00f/install-kolibrios-toolchain-action@main

      - name: Test toolchain working
        run: |
          kos32-gcc -v
          kos32-g++ -v
          kos32-ar -V 
          kos32-objcopy -V
          kos32-strip -V
```