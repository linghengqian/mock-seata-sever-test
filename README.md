## For https://github.com/apache/shardingsphere/issues/21347 and https://github.com/seata/seata/issues/5343

- Execute the following commands for comparison in Ubuntu 22.04.

```shell
sudo apt install unzip zip curl sed -y
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
sdk install java 22.3.1.r17-grl
sdk use java 22.3.1.r17-grl
sdk install maven

git clone git@github.com:linghengqian/mock-seata-sever-test.git
cd ./mock-seata-sever-test/

cd ./mock-seata-v142/
mvn clean test

cd ..
cd ./mock-seata-v161/
mvn clean test
```