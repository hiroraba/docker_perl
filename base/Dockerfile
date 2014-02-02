FROM base

RUN apt-get -y update
RUN apt-get -y install build-essential git-core curl
RUN apt-get clean

RUN git clone git://github.com/tokuhirom/plenv.git /root/.plenv
RUN git clone git://github.com/tokuhirom/Perl-Build.git /root/.plenv/plugins/perl-build/

RUN echo 'eval "$(plenv init -)"' >> /etc/profile.d/plenv.sh

ENV PATH /root/.plenv/bin:$PATH
ENV PLENV_ROOT /root/.plenv
RUN . /etc/profile
ADD ./perl_versions /root/
RUN xargs -L 1 plenv install < /root/perl_versions
