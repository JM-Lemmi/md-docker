# Moodle Downloader Docker Containers

This repository uses [Moodle-Downloader-2](https://github.com/C0D3D3V/Moodle-Downloader-2). There are two Docker containers in this repository, one for configuration and one for running. If you already have a config file, you can immediately use the moodle-downloader container.

## jmlemmi/moodle-downloader-config

This container will start the interactive configuration mode of the moodle-downloader package.

```bash
docker run -it -v ~/your/moodle/path:/config --rm jmlemmi/moodle-downloader-config
```

This will output the configuration file to ~/your/moodle/path.

You can also instead manually create the configuration file. Please see the [Moodle-Downloader Wiki](https://github.com/C0D3D3V/Moodle-Downloader-2/wiki/Config.json) for more information

## jmlemmi/moodle-downloader

This container will be downloading the content from moodle. It will need your config and in turn download to the specified volume.

```bash
docker run -d -v ~/your/moodle/paht:/srv/md jmlemmi/moodle-downloader
```