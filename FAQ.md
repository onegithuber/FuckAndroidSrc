### android complile error
[error1: ]
[ 77% 42873/55529] Building with Jack: out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/with-local/classes.dex
FAILED: out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/with-local/classes.dex 
/bin/bash out/target/common/obj/JAVA_LIBRARIES/framework_intermediates/with-local/classes.dex.rsp
Out of memory error (version 1.3-rc6 'Douarn' (441800 22a11d4b264ae70e366aed3025ef47362d1522bb by android-jack-team@google.com)).
Java heap space.

[soulution:]
export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx4g"
./prebuilts/sdk/tools/jack-admin kill-server
./prebuilts/sdk/tools/jack-admin start-server
