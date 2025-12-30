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
?? ref: https://www.reddit.com/r/pihole/comments/1gqi1hn/pihole_docker_on_ubuntu_issues_with_port_53_and/
```bash
sudo apt install systemd-resolved
sudo systemctl stop systemd-resolved
sudo systemctl disable systemd-resolved
sudo unlink /etc/resolved.conf
```
then do:
```bash
sudo nano /etc/systemd/resolved.conf        
```
change to:
```bash
DNS=8.8.8.8    
DNSStubListener=no
```
After edit the resolved.conf, do:
```bash
sudo systemctl daemon-reload
sudo systemctl enable systemd-resolved
sudo systemctl restart systemd-resolved
sudo systemd-analyze cat-config systemd/resolved.conf
```
