FROM httpd


RUN --mount=type=cache,target=/var/lib/apt,sharing=locked \
    --mount=type=cache,target=/var/cache/apt,sharing=locked \
    apt-get update && apt-get install -y \
       cpanminus \
       libssl-dev \
       gcc \
       zlib1g-dev \
       libnet-ssleay-perl \
       libio-socket-ssl-perl

# RUN cpanm install CGI LWP::UserAgent Net::SSLeay IO::Socket::SSL IO::Socket::SSL::Utils LWP::Protocol::https
# RUN cpanm install CGI LWP::UserAgent IO::Socket::SSL IO::Socket::SSL::Utils LWP::Protocol::https
RUN cpanm install CGI LWP::UserAgent
