# YouTube Channel Downloader Chart

This chart will deploy a number of cronjobs that will download the latest videos posted by whatever channels you like.

This project is very much a work-in-progress and breaking changes **WILL** be made. Stable versions will be released as the project progresses.

## Values File

To add new channels, simply add to the examples in the `values.yaml` file. The channel handle can be found in the channels homepage and always begin with an `@` symbol.

Additional customisation will be added.

## Using Locally with Minikube

Replace the first part of the `mount` command with whatever path you'd like the videos to end up in.

1. `minikube start`
2. `minikube mount $HOME/Movies/YouTube:/videos`
3. `helm upgrade --install channel-downloader .`

## Credits

The chart uses `yt-dlp` and the `youtube-dl` container by jeeaaasustest.