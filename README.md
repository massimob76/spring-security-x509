# notes

## create keystore

export DNAME_CA="CN=BaeldungCA,OU=baeldung.com,O=Baeldung,L=SomeCity,ST=SomeState,C=CC"
export KEYSTORE=keystore.jks
export PASSWORD=mykeystorepwd
keytool -genkey -alias ca -ext BC=ca:true -keyalg RSA -keysize 4096 -sigalg SHA512withRSA -keypass ${PASSWORD} -validity 3650 -dname ${DNAME_CA} -keystore ${KEYSTORE} -storepass ${PASSWORD}

## view keystore

keytool -list -v -keystore keystore.jks