FROM busybox
ENV HUGO_VERSION=0.55.5
RUN wget -O- https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz | tar zx

FROM alpine/git
ENTRYPOINT ["/hugo"]
COPY --from=0 /hugo /
