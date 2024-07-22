## Java笔记

使用Jre创建安卓证书

```sh

#方法1
keytool -genkey -alias 名称 -keyalg RSA -keysize 2048 -validity 36500 -keystore 名称.keystore
# 36500 是证书有效时间

#方法2
keytool -importkeystore -srckeystore 名称.keystore -destkeystore 名称.keystore -deststoretype pkcs12

```

