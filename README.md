# Overview

This is simple Qt daemon to automatically download [National University of Singapore](http://www.nus.edu.sg/)'s
[Integrated Virtual Learning Environment](http://ivle.nus.edu.sg/) workbin files.

You can read more about it [here](http://yjyao.com/2012/08/nus-ivle-downloader.html).

---

# How to use?

In order to compile the source code, You will need the Qt SDK 5.0+, which can be found [here](http://qt.nokia.com/products/qt-sdk/).

If you want to fork it into your own app, you may consider changing the APIKEY in the .pro file.

---

# Update: April 11th 2018

### [Download the updated version](https://github.com/luyangkenneth/IVLEDownloader/raw/master/IVLEDownloader.app.zip)

As the old API key has expired, I redeployed the app **(only macOS for now)** by following the steps from this [stackoverflow thread](https://stackoverflow.com/questions/19206462/compile-a-qt-project-from-command-line):

1. Replace the expired API key with a new one

See https://github.com/yyjhao/IVLEDownloader/issues/14

2. Run qmake on the project file to create a platform specific Makefile

```bash
qmake IVLEDownloader.pro
```

3. Compile program

```bash
make
```

This step also generated many other files, which I didn't figure why or how to prevent. I only committed the resulting `IVLEDownloader.app`.

### My machine environment
- macOS High Sierra 10.13.3
- Qt version 5.5.1, already installed beforehand via Homebrew
- Xcode version 9.3 (9E145), already installed beforehand
