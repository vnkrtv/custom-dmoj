# Custom DMOJ

## Configuring

### Judge server

There can be several judges in your system, so every judge has it's own JUDGE_NAME and JUDGE_KEY. Also wvwry judge try to cennect to running judge site, running on host JUDGE_SITE. To configure this settings, create environment file, like:
```
JUDGE_NAME=(Your judger's name)
JUDGE_KEY=(Your judger's key)
JUDGE_SITE=site_host
```
Put this file in config/judge.env
```
cd judge/.docker
```
### Online judge


## Installation

Get all repositories:
```
git clone https://github.com/vnkrtv/custom-dmoj.git && cd custom-dmoj
git pull --recurse-submodules
git submodule init
git submodule update --remote --recursive
```
Build judge docker image:
```
cp config/judge/entrypoint build/judge-server/.docker/entry
cd build/judge-server/.docker
sudo make judge-tier1
```
