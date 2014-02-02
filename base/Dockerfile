FROM base

RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get -y install git-core
RUN apt-get -y install wget
RUN apt-get -y install libopenssl-ruby
RUN apt-get -y install build-essential
RUN apt-get -y install libreadline-dev libssl-dev zlib1g-dev
RUN apt-get -y install libssl-dev libssl1.0.0
RUN apt-get -y install curl
RUN apt-get -y install libpq-dev
RUN apt-get -y install libsqlite3-dev

RUN git clone git://github.com/tokuhirom/plenv.git /root/.plenv
RUN git clone git://github.com/tokuhirom/Perl-Build.git /root/.plenv/plugins/perl-build/

RUN echo 'eval "$(plenv init -)"' >> /etc/profile.d/plenv.sh

ENV PATH /root/.plenv/bin:/root/.plenv/shims:$PATH
RUN /etc/profile
RUN plenv install 5.18.2
