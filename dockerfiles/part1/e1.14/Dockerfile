FROM ruby:2.6.0

COPY . .
RUN bundle install
RUN rails db:migrate
CMD rails s 