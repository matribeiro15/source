Notes - tech-source Ghost theme
===

Initial notes
---

### Build process

The original documenation says to run `yarn zip` to generate an uploadable zip file, which shows up as `dist/source.zip`. When I upload this to Ghost Pro, it shows up as an invalid theme. If I unzip `source.zip` and then zip the contents of the unzipped file, the resulting zip file is accepted as a valid theme. :confused: The file `rezipper.sh` does this work.

So, if the file generated by `yarn zip` isn't working, the following steps should create a valid file, at least on macOS:

```sh
$ yarn zip
$ ./rezipper.sh
```

This will generate a `dist/tech-source.zip` file, which is a valid Ghost Pro theme when generated on my system.