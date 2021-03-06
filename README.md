# si-ias-script
Manage IAS (integrated application server) programmatically (over CLI)

## Set PATH
```
export PATH=/QOpenSys/pkgs/bin:$PATH
```

## Set CLASSPATH
```
export CLASSPATH=/QIBM/ProdData/OS400/jt400/lib/jt400Native.jar:/QIBM/ProdData/OS/OSGi/shared/lib/iasadmin.jar
```

## Clone project
```
git clone https://github.com/jsranko/si-ias-script.git
```

## Configure and create server
Change the base configuration 
```
nano createServer.properties
```
und then create the server
```
java com.ibm.lwi.admin.IntegratedServerAdmin -createServer createServer.properties
```

## Install applicaiton
Install your application. For example:
```
wget -O /tmp/SampleWebApp.war https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war
```
Now install you war file application:
```
java com.ibm.lwi.admin.IntegratedServerAdmin -installApplication IASTEST1 /tmp/SampleWebApp.war
```

## Start applicaiton
```
java com.ibm.lwi.admin.IntegratedServerAdmin -startApplication IASTEST1 SampleWebApp
```

## Remove server
### Remove server by Name
```
java com.ibm.lwi.admin.IntegratedServerAdmin -removeServerByName IASTEST1
```

## Start server

```
java com.ibm.lwi.admin.IntegratedServerAdmin -startServer IASTEST1
```

## Stop server

```
java com.ibm.lwi.admin.IntegratedServerAdmin -stopServer IASTEST1
```

## Stop applicaiton
```
java com.ibm.lwi.admin.IntegratedServerAdmin -stopApplication IASTEST1 SampleWebApp
```

## Remove applicaiton
```
java com.ibm.lwi.admin.IntegratedServerAdmin -removeApplication IASTEST1 SampleWebApp
```
