InstallCert
===========

Fork of Andreas Sterbenz's InstallCert.java from Google Code@https://code.google.com/p/java-use-examples/source/browse/trunk/src/com/aw/ad/util/InstallCert.java

Compiling
---------

1. Download/Install Java
2. Ensure java (java.exe for Windows) is in the system path
3. Run "javac InstallCert.java"

Use
---

1. Run "java InstallCert host[:port]"
2. The program should show an SSL exception and will present the server-sent certificates. Choose the appropriate one to add to the keystore 'jssecacerts' in the current directory. Copying this file into JAVA_HOME/jre/lib/security as is will trust the cert for all JSSE apps. Copying into the directory by overwriting the cacerts file will cause all java apps to trust the new certificate.
3. The trust chain can be verified by re-running "java InstallCert host:[port]"

A more detailed explanation can be found at: https://java.net/projects/javamail/pages/InstallCert

Also, a version of this code with STARTTLS support (which I have not tested) can be found at: http://s-n-ushakov.blogspot.com/2013/11/yet-another-installcert-for-java-now.html

