# parent-pom

1. publish the pom.xml to exchange and consume it using the co-ordinates in the consumer application
2. edit the settings.xml with the connected app credentials and place it in the maven conf installation path
3. Place this <parent> tag on top
 <parent>
    <groupId>[org id]</groupId>
    <artifactId>parent-pom</artifactId>
    <version>1.0.0</version>
  </parent>
4. Place the following <repository> tag as well in the consumer applications
   <repository>
     <id>my.anypoint.credentials</id>
     <name>Corporate Repository</name>
     <url>https://maven.anypoint.mulesoft.com/api/v2/organizations/[org id]/maven</url>
     <layout>default</layout>
   </repository>

credits: https://effinium.com/parent-pom-in-mule/
         https://help.salesforce.com/s/articleView?id=001116554&type=1
