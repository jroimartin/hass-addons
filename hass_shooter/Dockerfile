From golang:1.17-buster

RUN apt-get update && \
	apt-get --yes --no-install-recommends install chromium imagemagick && \
	apt-get clean

RUN go install github.com/jroimartin/hass-shooter@v0.3.0

ENTRYPOINT ["/go/bin/hass-shooter"]
CMD ["-c", "/data/options.json"]
