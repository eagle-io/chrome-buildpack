# Chrome Buildpack

A [Cloud Native Buildpack](https://buildpacks.io/) that installs the latest version of Chrome for Linux AMD64.


## Usage

Build with defaults:

```
$ pack build --buildpack eagle-io/chrome-buildpack myapp
```

---

### Environment variables

Optionally set these environment variables during build to change defaults

* Set the channel to install chrome from:
  * `BP_CHROME_CHANNEL` = `stable` | `beta` | `unstable` (default: stable)
  
* Install required dependencies:
  * `BP_CHROME_INSTALL_DEPS` = `true` (default: false)
  
* Force reset cache between rebuilds and reduce layer size
  * `BP_CHROME_NO_CACHE` = `true` (default: false)

<br />

Build with required dependencies:
```
$ pack build --buildpack eagle-io/chrome-buildpack --env BP_CHROME_INSTALL_DEPS=true myapp
```

---
## License

MIT
