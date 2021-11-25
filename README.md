# docker-sidekiq-web

A Docker setup to run a stand-alone instance of the Sidekiq UI.

## Setup

`cp .env_sample .env` change the environment variables as required

use IRB to create a .session.key
`require 'securerandom'; File.open(".session.key", "w") {|f| f.write(SecureRandom.hex(32)) }`

## Usage

`docker-compose up`

or

`docker build -t sidekiq_web .`

`docker run -d --rm --env-file=.env --name sidekiq_web -p 3030:3030 sidekiq_web`
