## Sail install
```
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php82-composer:latest \
    composer install --ignore-platform-reqs
```

## Sail command shortcut
```
# ~/.bashrcにエイリアスを追加する。
vi ~/.bashrc
# 以下を末尾に追加
alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'
```
