# ghc-build-scripts
Script collection for building ghc cross compiler for mobile development

# building mobile ghc(s)
The `build-mobile-ghcs` script is supposed to be use as follows:

`ghc $ path/to/ghc-build-scripts/build-mobile-ghcs /prefix/path/mobile-ghc /path/to/libiconv /path/to/clang`

And requires <https://github.com/angerman/ghc-ios-scripts> to be in `$PATH`, as well as having libiconv built for
both android platforms (iOS comes with libiconv).  Also path/to/clang should be a rather recent (read patched)
clang for iOS to work without the need to disable `-dead_strip`. Running the script takes about an hour on my iMac,
ymmv.

and will result in ghcs for:

| Name                         | Platform          |
| ---------------------------- | ----------------- |
| aarch64-apple-darwin14       | iOS/64bit arm     |
| armv7-none-linux-androiedabi | Android/32bit arm |
| aarch64-none-linux-android   | Android/64bit arm |
