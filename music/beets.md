
# Beets

> Music library manager and MusicBrainz tagger.

- [beets.io](http://beets.io/)

---

## Links & Resources

- [`beetbox/beets`](https://github.com/beetbox/beets)
  - [Getting Started](https://beets.readthedocs.io/en/stable/guides/main.html)
  - [AutoTagger](https://beets.readthedocs.io/en/stable/guides/tagger.html)
  - [Configuration](https://beets.readthedocs.io/en/stable/reference/config.html)
  - [Advanced Awesomeness](https://beets.readthedocs.io/en/stable/guides/advanced.html)
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

## Basic Usage

Beets’ tagger is invoked using the `beet import` command.

Music should be organized by album into directories. That is, the tagger assumes that each album is in a single directory. These directories can be arbitrarily deep, but any directory with music files in it is interpreted as a separate album.

Useful command line options:

- `beet import -s`: run in singleton mode, tagging individual tracks instead of whole albums at a time.

Import choices:

- **A**: Apply the suggested changes shown and move on.
- **M**: Show more options.
- **S**: Skip this album entirely and move on to the next one.
- **U**: Import the album without changing any tags.
- **T**: Import the directory as singleton tracks, not as an album.
- **G**: Group tracks in this directory by album artist and album and import groups as albums. If the album artist for a track is not set then the artist is used to group that track.
- **E**: Enter an artist and album to use as a search in the database.
- **I**: Enter a metadata backend ID to use as search in the database.
- **B**: Cancel this import task altogether. No further albums will be tagged; beets shuts down immediately.

---

## Configuration

Configuration file location: `%APPDATA%\beets\config.yaml`

- `beet config -p` to find config file location.
- `beet config -e` to open config file in text editor.
  - Note: `%EDITOR%` environment variable must be set.

### Plugins

- [Discogs](https://beets.readthedocs.io/en/stable/plugins/discogs.html)
- [FromFilename](https://beets.readthedocs.io/en/stable/plugins/fromfilename.html)

[]()

- [Chromaprint](https://beets.readthedocs.io/en/stable/plugins/chroma.html)
- [Edit](https://beets.readthedocs.io/en/stable/plugins/edit.html)
- [EmbedArt](https://beets.readthedocs.io/en/stable/plugins/embedart.html)
- [FetchArt](https://beets.readthedocs.io/en/stable/plugins/fetchart.html)

[]()

- [LastGenre](https://beets.readthedocs.io/en/stable/plugins/lastgenre.html)
- [Lyrics](https://beets.readthedocs.io/en/stable/plugins/lyrics.html)
- [Web](https://beets.readthedocs.io/en/stable/plugins/web.html)

---
