## Instructions

- open a bash shell (if on windows use git bash, WSL, or any shell configged for bash commands)
- execute build command from same folder as docker file
- exectute run command
- get the log tail and navigate to the last url displayed

# Docker Build and Run Commands

### Build

```bash
docker build -t jupsparkexp -f Dockerfile_jupsparkexp .
```

### Run

```bash
docker run -d --rm -p 8888-8889:8888-8889 jupsparkexp 
```

### Exec into a shell
```bash
docker exec -it <first 4 containerid> bash
```

### Viewing Logs

Get the tail
```bash
docker logs <first 4 containerid>
```

Get continuous logs

```bash
docker logs --follow <fist 4 container id>
```
