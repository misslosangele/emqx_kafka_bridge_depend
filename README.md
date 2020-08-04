# emqx_kafka_bridge_depend
# otp_src
tar -zxvf otp_src_21.3.tar.gz
cd otp_src_21.3
./otp_build autoconf

./configure --enable-smp-support--enable-threads --enable-sctp --enable-kernel-poll --enable-hipe --with-ssl
make && make install

# rebar3
cd rebar3
./bootstrap
./rebar3 local install
