FROM ruby:2.6.0

# Install required packages using Ubuntu repositories
RUN apt-get update -qq && \
    apt-get install -y build-essential libpq-dev nodejs

# Set the working directory
WORKDIR /app

# Copy Gemfiles
COPY Gemfile Gemfile.lock ./

# Install gems
RUN bundle install

# Copy the rest of the application code
COPY . .

# Define the default command to run the application
CMD ["./bin/d_cmd.sh"]
