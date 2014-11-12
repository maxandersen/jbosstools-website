FROM goldmann/awestruct

WORKDIR /home/awestruct

ENV HOME /home/awestruct
ENV RUBY_VERSION 1.9.3
ENV AWESTRUCT_VERSION 0.5.5

ADD ./Gemfile Gemfile
ADD ./Gemfile.lock Gemfile.lock

RUN bash -l -c "rvm install $RUBY_VERSION"
RUN bash -l -c "rvm use $RUBY_VERSION"
RUN bash -l -c "rvm gemset create jbosstools-website"
RUN bash -l -c "gem install bundler"
RUN bash -l -c "bundle install"

EXPOSE 4242

CMD ["bash", "--login"]

