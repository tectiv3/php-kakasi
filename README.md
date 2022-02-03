##### php-kakasi For PHP 7.2+

Tested on PHP 8.1

#### If you install dockerd on your computer, you can check quickly.

```bash
$ git clone https://github.com/helloooideeeeea/php-kakasi.git
$ cd php-kakasi
$ docker build -t php -f docker/Dockerfile docker/
$ docker run -it -v $(pwd):/home/ec2-user/develop/ php:latest /bin/bash
```

#### Without docker

- Compile extension
```bash
git clone https://github.com/tectiv3/php-kakasi.git && cd php-kakasi/kakasi && phpize && autoconf -f && ./configure && make && make install
```
- Add `extension=kakasi.so` to php.ini

#### Test

```
php test.php 
array(4) {
  ["base"]=>
  string(15) "狩野達也君"
  ["hira"]=>
  string(21) "かのたつやくん"
  ["kata"]=>
  string(21) "カノタツヤクン"
  ["alph"]=>
  string(14) "kanotatsuyakun"
}
```
