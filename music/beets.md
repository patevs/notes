
# Beets

> Music library manager and MusicBrainz tagger.

- [beets.io](http://beets.io/)

---

## Links & Resources

- [`beetbox/beets`](https://github.com/beetbox/beets)
  - [Getting Started](https://beets.readthedocs.io/en/stable/guides/main.html)
  - [Configuration](https://beets.readthedocs.io/en/stable/reference/config.html)
  - [AutoTagger](https://beets.readthedocs.io/en/stable/guides/tagger.html)
  - [Plugins](https://beets.readthedocs.io/en/stable/plugins/index.html)

---

## Install & Setup

1. Download and install `python3` and `pip`

    ```powershell
    # Install with chocolately
    $ choco install python3 -y
        # Verify python and pip installations
    $ python -V
    # Python 3.7.3
    $ python -m pip -V # or $ pip -V
    # pip 19.0.3
    ```

2. Download and install `beets`

    ```powershell
    # Install with pip
    $ python -m pip install beets
    # Verify installation
    $ beet --version
    # beets version 1.4.9
    ```

3. Configure `beets`

    ```powershell
    # Show config location
    $ beet config -p
    # Edit config
    $ beet config -e
    ```

---
