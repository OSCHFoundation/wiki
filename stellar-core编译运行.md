# Ubuntu系统 16.04
* sudo add-apt-repository ppa:ubuntu-toolchain-r/test
* sudo apt-get update
* sudo apt-get install git build-essential pkg-config autoconf automake libtool bison flex libpq-dev clang++-5.0 gcc-5 g++-5 cpp-5 curl
* sudo apt-get install pandoc
* sudo apt-get install postgresql
* sudo apt-get install pgadmin3

# 配置postgres远程连接
* sudo su postgres
* psql postgres
* ALTER USER postgres with PASSWORD 'postgres' 
* \q
* sudo vim /etc/postgresql/9.5/main/postgresql.conf
* listen_addresses = ‘localhost’改为 listen_addresses = ‘*’
* #password_encryption = on 改为 password_encryption = on
* sudo vim /etc/postgresql/9.5/main/pg_hba.conf
* 添加 host all all 0.0.0.0/0 md5
* /etc/init.d/postgresql restart #重启postgresql
* psql -U postgres -h 127.0.0.1 测试登入

# 下载源码编译
* git clone -b prod https://github.com/OSCHFoundation/osch-core.git
* cd stellar-core
* git submodule init
* git submodule update

# 源码编译
* ./autogen.sh
* ./configure
* make （配置好可以尝试 make -j 配置差切莫尝试）
* make check
* sudo make install
* 复制一下配置内容到stellar-core下面 https://github.com/stellar/docker-stellar-core-horizon/blob/master/testnet/core/etc/stellar-core.cfg * 修改里面的数据库用户名密码

# horizon下载配置
* 浏览器进入https://github.com/stellar/go/tree/master/services/horizon  页面下方找到horizon-linux-amd64点击下载
* tar zxvf horizon-v0.11.0-linux-amd64
* 配置方法参考地址：https://github.com/stellar/go/blob/master/services/horizon/internal/docs/reference/admin.md#configuring


# 创建数据库
* 打开pgadmin3
* 新建2个数据库horizon和soch2.0
* 建立stellar表：stellar-core --newdb
* 建立本地历史：stellar-core --newhist local

# 运行osch-core
* stellar-core --forcescp
* stellar-core

# 启动horizon
* 在.bashrc中添加环境变量： vim ~/.bashrc
export DATABASE_URL="postgresql://user:pass@localhost/horizon2.1"  
export STELLAR_CORE_DATABASE_URL="postgresql://user:pass@localhost/stellar2.1?sslmode=disable"  
export STELLAR_CORE_URL="http://localhost:11626"  
export HISTORY_RETENTION_COUNT=1000  
export INGEST="true"  
修改上述用户名密码和数据库  
使环境变量生效：source ~/.bashrc  
* 初始化horizon数据库：进入horizon目录下 ./horizon db init 初始化数据库
* ./horizon
