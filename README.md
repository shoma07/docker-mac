# Docker Mac

Scripts for using docker on mac without Docker Desktop

This script uses multipass to launch and manage the vm.

Docker Ddesktop automatically exposes the port of the vm to the host, but this script explicitly port forwards it.

## Installation

Install it yourself as:

```sh
$ curl -fL https://raw.githubusercontent.com/shoma07/docker-mac/main/bin/docker-mac > /usr/local/bin/docker-mac
$ chmod +x /usr/local/bin/docker-mac
```

## Usage

```sh
$ docker-mac help
```

```sh
# install dependences
$ docker-mac install

# create and start vm
## docker-mac create -c <cpus> -m <mem> -d <disk>
$ docker-mac create -c 3 -m 8G -d 64G

# destroy vm
$ docker-mac destroy

# start vm
$ docker-mac start

# stop vm
$ docker-mac stop

# restart vm
$ docker-mac restart

# expose port from vm to host
$ docker-mac expose 3000

# unexpose port from vm to host
$ docker-mac unexpose 3000
```

You can use the docker and docker compose commands while the VM is booting.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/docker-mac.

## License

[MIT License](https://opensource.org/licenses/MIT)
