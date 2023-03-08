## Тут немного инфы о том, как я тестировал Crypto в нашем проекте и что имеет ся сейчас:

* В Messenger-project/Crypto-libs/botan-master лежат исходники библиотеки Botan.
  * Её можно собрать следуя инструкции, находясь в src:
    * [./../Crypto-libs/botan-master/configure.py](..%2F..%2FCrypto-libs%2Fbotan-master%2Fconfigure.py)
    * make
    * make check
    * sudo make install (можно без sudo, но тогда надо дать права)
  * Установка пройдет, надо запомнить куда поставились пакеты, скорее всего что-то такое: "/usr/local/include/botan-3" там лежит папочка botan
  * Больше можно почитать в [Crypto-libs/botan-master/readme.rst](..%2F..%2FCrypto-libs%2Fbotan-master%2Freadme.rst)
* Сейчас (после установки и сборки либы) можно запустить [Botan-Test-1.cpp](CryptoTest%2FBotan-Test-1.cpp).
  * `g++-12 Botan-Test-1.cpp -o Botan-Test-1 -std=c++20 -l:libbotan-3.a -I/usr/local/include/botan-3`
    * Возможно, вместо `-I/usr/local/include/botan-3` надо указывать другой пусть, если у вас папка с либой другая.

