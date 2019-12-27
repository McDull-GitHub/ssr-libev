# ssr-libev

## Installation

### # Debian / Ubuntu

```
apt-get install git build-essential autoconf libtool libssl-dev  libpcre3 libpcre3-dev asciidoc xmlto zlib1g-dev libsodium-dev
git clone https://github.com/McDull-GitHub/ssr-libev.git
cd ssr-libev
./configure --prefix=/usr/local/SSR --disable-documentation
make -j4
make install
```

## Usage

#### -> Create a SSR Config
```
mkdir /usr/local/SSR/conf
vim /usr/local/SSR/conf/SSR-Config.json
```

##### SSR-Config.json Demo
```
{
  "method" : "rc4-md5",
  "server" : "server.com",
  "timeout" : 60,
  "protocol_param" : "protocol.com",
  "protocol" : "origin",
  "local_port" : 1086,
  "server_port" : 12345,
  "local_address" : "127.0.0.1",
  "obfs" : "http_simple",
  "obfs_param" : "obfs.com",
  "password" : "password"
}
```

#### -> Run
```
/usr/local/SSR/ss-local -c /usr/local/SSR/SSR-Config.json
```
#### -> Stop

```
Control(Ctrl) + C
```

##### Shell Export Command

```
export http_proxy=http://127.0.0.1:1086;
export https_proxy=http://127.0.0.1:1086;
export all_proxy=socks://127.0.0.1:1086;
```
