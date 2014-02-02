FROM base

RUN apt-get -y update
RUN apt-get -y install build-essential git-core curl
RUN apt-get clean

RUN git clone git://github.com/tokuhirom/plenv.git /root/.plenv
RUN git clone git://github.com/tokuhirom/Perl-Build.git /root/.plenv/plugins/perl-build/

RUN echo 'eval "$(plenv init -)"' >> /etc/profile.d/plenv.sh

ENV PATH /root/.plenv/bin:$PATH
RUN . /etc/profile
RUN plenv install 5.18.2
