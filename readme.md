# Sources:
Flaresolverr: https://github.com/FlareSolverr/FlareSolverr
jackett: https://hub.docker.com/r/linuxserver/jackett

## Tonton Jo  
### Join the community:
[![Youtube channel](https://github-readme-youtube-stats.herokuapp.com/subscribers/index.php?id=UCnED3K6K5FDUp-x_8rwpsZw&key=AIzaSyA3ivqywNPQz0xFZBHfPDKzh1jFH5qGD_g)](http://youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw?sub_confirmation=1)
[![Discord Tonton Jo](https://badgen.net/discord/members/N3ssTdTS?label=Discord%20Tonton%20Jo%20&icon=discord)](https://discord.gg/N3ssTdTS)
### Support the channel with one of the following link:
[![Ko-Fi](https://badgen.net/badge/Buy%20me%20a%20Coffee/Link?icon=buymeacoffee)](https://ko-fi.com/tontonjo)
[![Infomaniak](https://badgen.net/badge/Infomaniak/Affiliated%20link?icon=K)](https://www.infomaniak.com/goto/fr/home?utm_term=6151f412daf35)
[![Express VPN](https://badgen.net/badge/Express%20VPN/Affiliated%20link?icon=K)](https://www.xvuslink.com/?a_fid=TontonJo)  


## Flaresolverr
```shell
docker run -d \
  --name=flaresolverr \
  -p 8191:8191 \
  -e LOG_LEVEL=info \
  -e CAPTCHA_SOLVER=harvester \
  -e HARVESTER_ENDPOINT=https://127.0.0.1:5000/token \
  --restart unless-stopped \
  ghcr.io/flaresolverr/flaresolverr:latest
```
  
## Jackett:
```shell
docker run -d \
  --name=jackett \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Europe/London \
  -p 9117:9117 \
  -v <path to data>:/config \
  -v <path to blackhole>:/downloads \
  --restart unless-stopped \
  ghcr.io/linuxserver/jackett
```
