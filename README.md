# si-ias-script
Manage IAS (integrated application server) programmatically (over CLI)

## Set CLASSPATH
```
export CLASSPATH=/QIBM/ProdData/OS400/jt400/lib/jt400Native.jar:/QIBM/ProdData/OS/OSGi/shared/lib/iasadmin.jar
```

## Create server

```
java com.ibm.lwi.admin.IntegratedServerAdmin -createServer createServer.properties
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

## Install applicaiton

```
java com.ibm.lwi.admin.IntegratedServerAdmin -stopServer IASTEST1
```
