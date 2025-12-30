# env

## Docker
> Installation - check official website
> CLI
```bash
brew install docker docker-compose
```
```bash
docker-compose up -d
```

## Nvim 
> symlink nvim config folder 
```bash
ln -s $(pwd)/.config/nvim ~/.config/nvim
```

## Tmux
soft link
```bash
ln $(pwd)/.tmux.conf ~/.tmux.conf
```

## Pi-hole
? fix port 53 in usage
- not sure which solution is correct
?? https://docs.pi-hole.net/docker/tips-and-tricks/
?? ref: https://www.reddit.com/r/pihole/comments/1gqi1hn/pihole_docker_on_ubuntu_issues_with_port_53_and/
