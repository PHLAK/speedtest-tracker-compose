Requirements
------------

  - [Docker](https://www.docker.com)
    - [Docker Compose](https://docs.docker.com/compose/)
  - [GNU Make](https://www.gnu.org/software/make/) (optional)

Installation
------------

  1. Clone the repository

          git clone https://github.com/PHLAK/speedtest-tracker-compose.git

  2. Initialize the configuration files

           make init

  3. Set the environment variables in `.env`

  4. Run `docker compose config` to validate and confirm your configuration

  5. Run `docker compose up -d` to start the containers

Configuration
-------------

Your installation can be configured by defining environment variables in the
`environment.d/*.env` files. Reference the documentation for the individual
apps for available environment variables and their purpose.

> [!IMPORTANT]
> After modifying files in `environment.d` you must restart your containers
> (i.e. `docker compose up -d`) for the changes to apply.

Updating
--------

  1. Fetch latest file changes from the repository

         git pull --ff-only

  2. If necessary, initialize new configuration files

         make init

  3. Pull new images and restart containers

         docker compose pull
         docker compose up -d
