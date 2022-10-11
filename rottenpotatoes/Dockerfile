# ruby version
FROM ruby:2.6.6
# \ is next line
RUN apt-get update -qq && apt-get -y install \
    build-essential nodejs sqlite3 libsqlite3-dev
# create path in docker
WORKDIR /softeng/hw-bdd
# copy Gemfile to ./ -> (/softeng/hw-bdd)
COPY Gemfile ./
# Run this command in container
# Auto Run
# install bundler and Gemfile
RUN gem install bundler:2.0.0.pre.3 && bundle install
# first dot is my dir , second . is dir in docker
COPY . .
# using cmd in docker
# goto terminal in docker
CMD ["/bin/bash","-c","bash"]
