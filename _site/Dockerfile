FROM ubuntu:18.04

RUN apt-get update && \
    apt-get install -y ruby-full && \
    apt-get install -y build-essential && \
    apt-get install -y zlib1g-dev && \
    apt-get clean

RUN echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
RUN echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
RUN echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc

RUN gem install jekyll bundler

RUN mkdir /software-portal-web
COPY . /software-portal-web

WORKDIR /software-portal-web

RUN apt-get autoclean
RUN apt-get autoremove

RUN gem update --system
RUN bundle install

CMD ["bundle", "exec", "jekyll", "serve"]
