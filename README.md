# Fuzzapi

Fuzzapi is rails application which uses API_Fuzzer and provide UI solution for gem.

# Setup

1. Install ruby in your machine using [rvm](https://rvm.io/rvm/install) and [rbenv](https://gorails.com/setup/ubuntu/20.04)

2. Clone the repository into your machine

       cd /usr/share/ && git clone https://github.com/4k4xs4pH1r3/fuzzapi.git && cd /usr/share/fuzzapi/ && mkdir -p app/assets/config && echo '{}' > app/assets/config/manifest.js && cd /usr/share/fuzzapi/bin

3. Install & update fuzzapi gem dependencies [ruby 2.7.1](https://www.ruby-lang.org/en/downloads/releases/) + [rails 6.0.2.2](https://rubygems.org/gems/rails/versions)

       rvm install 2.7.1 && rvm use 2.7.1 && gem install rails -v 6.0.2.2 && rbenv rehash && bundle update && gem install API_Fuzzer && gem install rubygems-update && update_rubygems && gem update --system && sudo gem update && gem update `gem outdated | cut -d ' ' -f 1` && bundle install && rails -v && ruby -v && rvm -v && rbenv -v

5. `rake db:migrate` to create tables, migrations etc.

6. `rails s` to run the server and run `export REDIS_URL=redis://127.0.0.1:6379/0 && bundle exec sidekiq` to run sidekiq.

7. Open `http://localhost:3000` in browser which should point to the application url
#
#
#

## Docker

Fuzzapi comes with `Docker` to simplify installation processing. Following commands will setup application using `Docker`.

1. Install ruby in your machine using [rvm](https://rvm.io/rvm/install) and [rbenv](https://gorails.com/setup/ubuntu/20.04)

2. Clone the repository into your machine

        cd /root && git clone https://github.com/4k4xs4pH1r3/fuzzapi.git && cd /root/fuzzapi/ && mkdir -p app/assets/config && echo '{}' > app/assets/config/manifest.js && cd /root/fuzzapi/bin

3. Install & update fuzzapi gem dependencies [ruby 2.7.1](https://www.ruby-lang.org/en/downloads/releases/) + [rails 6.0.2.2](https://rubygems.org/gems/rails/versions)

       rvm install 2.7.1 && rvm use 2.7.1 && gem install rails -v 6.0.2.2 && rbenv rehash && bundle update && gem install API_Fuzzer && gem install rubygems-update && update_rubygems && gem update --system && sudo gem update && gem update `gem outdated | cut -d ' ' -f 1` && bundle install && rails -v && ruby -v && rvm -v && rbenv -v

3. Install Docker in your local machine

4. Run `docker-compose build` to build the image locally.

5. Run `docker-compose up` to run the server.

6. Open `http://localhost:3000` in browser which should point to the application url



Fuzzapi uses [API_Fuzzer](https://github.com/lalithr95/API-Fuzzer) gem.

Authors:
www.twitter.com/abhijeth;
www.twitter.com/lalithr95;
www.twitter.com/srini0x00


### New Scan
<img width="1679" alt="scan body" src="https://cloud.githubusercontent.com/assets/4562611/19390428/12224610-91f6-11e6-9ece-6e3cd7dd35ea.png">

### Scan Result
<img width="1679" alt="scan" src="https://cloud.githubusercontent.com/assets/4562611/19390442/1ef2f3d0-91f6-11e6-91eb-640b17d64a0b.png">

### Scan Histoy
<img width="1679" alt="scan2" src="https://cloud.githubusercontent.com/assets/4562611/19390533/79f83b96-91f6-11e6-9476-c3093b809674.png">
