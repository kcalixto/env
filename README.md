# env

## Munin
? description
```
Munin is a networked resource monitoring tool that can help 
analyze resource trends and "what just happened to kill our performance?" 
problems. It is designed to be very plug and play. A default installation 
provides a lot of graphs with almost no work.
```

> ~/etc/munin/munin-node.conf
```
allow ‘^127.’
allow ‘^192.0.2.1$’
```

> /etc/munin/munin.conf
```
[node01.example.com]
    address 192.0.2.4

[node02.example.com]
    address node02.example.com

[node03.example.com]
    address 2001:db8::de:caf:bad
```

? restart service
```
sudo service munin-node restart
```

## Tmux
clone tmux plugin manager
```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
soft link
```
ln .tmux.conf ~/.tmux.conf
```
