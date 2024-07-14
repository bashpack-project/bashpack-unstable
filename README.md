> [!CAUTION]
> **This repository is intended for development and testing purposes.**\
> Stable releases are available at https://github.com/bashpack-project/bashpack

# Bashpack unstable & dev

### Quick start

**Install**
_The first installation will always be on the main publication. You'll have to manually switch between publication stages._ \
_Explaination below._

```javascript
curl -sL https://raw.githubusercontent.com/bashpack-project/bashpack/main/bashpack.sh -o bashpack.sh \
 && chmod +x bashpack.sh \
 && sudo ./bashpack.sh -i \
 && rm bashpack.sh
```

**Uninstall**
```javascript
sudo bp --self-delete
```

**Usage**
```javascript
bp --help
```

<br>

### Switch between repositories
To switch between repositories, you have to edit the "publication" parameter in /etc/bashpack/bashpack_config \ 
Following values can be used: \
- main \
- unstable \
- dev \

**main to unstable**
```javascript
sudo sed -i 's/main/unstable/g' /etc/bashpack/bashpack_config \
 && sudo bp -u
```

**main to dev**
```javascript
sudo sed -i 's/main/dev/g' /etc/bashpack/bashpack_config \
 && sudo bp -u
```

**unstable to dev**
```javascript
sudo sed -i 's/unstable/dev/g' /etc/bashpack/bashpack_config \
 && sudo bp -u
```

**dev to unstable**
```javascript
sudo sed -i 's/dev/unstable/g' /etc/bashpack/bashpack_config \
 && sudo bp -u
```

<br>
