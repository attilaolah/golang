FROM golang:1.4

RUN git clone git://github.com/golang/go /usr/src/go1.5 \
	&& cd /usr/src/go1.5/src \
	&& GOROOT_BOOTSTRAP=/usr/src/go GOROOT_FINAL=/usr/src/go ./make.bash \
	&& rm -rf /usr/src/go1.5/.git /usr/src/go \
	&& mv /usr/src/go1.5 /usr/src/go

COPY go-wrapper /usr/local/bin/
