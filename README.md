# Next.js 14 Development Docker Container

A ready-to-use Docker setup for developing Next.js 14 frontend applications. This project provides a simple and efficient way to run your Next.js app in a containerized development environment, making onboarding and local development easier for all team members.

## Features

- Docker Compose configuration for local development
- Customizable environment variables
- Hot-reloading support with volume mounts
- User and permissions handling for smooth file access
- Makefile for common Docker commands

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)
- (Optional) [GNU Make](https://www.gnu.org/software/make/) for using the provided Makefile

### Usage

1. Clone this repository:
	```bash
	git clone https://github.com/chamod-randeni/docker-continer-for-nextjs-applciation.git
	cd docker-continer-for-nextjs-applciation/docker-for-next
	```

2. Update the `.env` file if needed (default values are provided).

3. Start the development container:
	```bash
	make up-f
	```
	or (to run in detached mode):
	```bash
	make up
	```

4. Access your Next.js app at [http://localhost:3001](http://localhost:3001) (or the port specified in `.env`).

5. To stop the container:
	```bash
	make down
	```

6. To open a shell inside the running container:
	```bash
	make shell-app
	```

## Project Structure

- `docker-for-next/docker-compose-dev.yml`: Docker Compose configuration for development
- `docker-for-next/dockerfiles/dev.Dockerfile`: Dockerfile for the development environment
- `docker-for-next/.env`: Environment variables for Docker Compose
- `docker-for-next/Makefile`: Helper commands for Docker operations
- `src/`: Your Next.js application source code

## Notes

- This setup is intended for development only. Do not use it in production.
- The container mounts your local `src/` directory for live code updates.
- Node modules are mounted as a volume to persist dependencies between runs.

## Contributing

Feel free to open issues or submit pull requests to improve this setup for the community!

## License

MIT

---