OpenSSL1.0.1cForAndroid
=======================
1、在openssl的jni目录下的Application.mk中增加：

APP_PLATFORM := android-8

2、在openssl根下的android-config.mk中增加：

APP_ABI := armeabi armeabi-v7a

3、crypto/Android.mk 大约535行，添加：

LOCAL_EXPORT_LDLIBS := -lz

注意有没添加以下两个静态库，大约576行，添加(暂时不用)：

LOCAL_LDLIBS := -lz –ldl


OpenSSL 1.0.1c For Android
