FROM ruby:2.3.6-alpine3.4
RUN apk add --no-cache libc-dev sqlite-dev gcc make git nodejs && \
    git clone https://github.com/gothinkster/rails-realworld-example-app.git && \
    cd rails-realworld-example-app/ && \
    echo gem \'tzinfo-data\' >> Gemfile && \
    bundle install && \
    rake db:migrate 

ADD ./cors.rb /rails-realworld-example-app/config/initializers/cors.rb
WORKDIR rails-realworld-example-app/
CMD [ "rails", "s", "-b", "0.0.0.0" ]
EXPOSE 3000
