## Install

#### 1. update

```
sudo apt-get update
```

#### 2. install https connection packages

```
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
```

#### 3. add GPG key

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

#### 4. register docker repository

```
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

#### 4-1. retry update

```
sudo apt-get update
```

#### 5. install docker

```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

#### 6. check docker

```
sudo docker version
```

#### 7. use docker without 'sudo'

```
sudo usermod -aG docker $USER
```

#### 8. system reboot

```
reboot
```
