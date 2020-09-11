# R

This is a R engine for running R apps with [Nanobox](http://nanobox.io).

## Usage
To use the R engine, specify `r` as your `engine` in your boxfile.yml

```yaml
run.config:
  engine: r
```

## Build Process
When [running your app](https://docs.nanboox.io/cli/run/), this engine compiles code by doing the following:

- `yarn install`

## Configuration Options
This engine exposes configuration options through the [Boxfile](http://docs.nanobox.io/boxfile/), a yaml config file used to provision and configure your app's infrastructure when using Nanobox.

#### Overview of Boxfile Configuration Options
```yaml
run.config:
  engine: r
  engine.config:
    runtime: r-4.4
    dep_manager: yarn
    python_version: python-2.7
```

---

#### runtime
Specifies which R runtime and version to use. The following runtimes are available:

- r-0.8
- r-0.10
- r-0.12
- r-4.8
- r-5.12
- r-6.11
- r-7.10
- r-8.6
- r-8.9

```yaml
run.config:
  engine: r
  engine.config:
    runtime: r-8.6
```

---

#### dep_manager
Specifies whether the engine should use npm or yarn to fetch R modules. Defaults to `yarn`.

```yaml
run.config:
  engine.config:
    dep_manager: yarn
```

#### python_version
Specifies the version of Python to install with the following available values:

- python-2.7
- python-3.4
- python-3.5
- python-3.6 (Default)

```yaml
run.config:
  engine.config:
    python_version: python-2.7
```



---

## Help & Support
This is a generic (non-framework-specific) R engine provided by [Nanobox](http://nanobox.io). If you need help with this engine, you can reach out to us in the [#nanobox IRC channel](http://webchat.freeR.net/?channels=nanobox). If you are running into an issue with the engine, feel free to [create a new issue on this project](https://github.com/pagodabox/nanobox-engine-R/issues/new).
