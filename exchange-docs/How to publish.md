# How to publish into a new project

**Note**

> Make sure that you have already maven configured in your machine.

- Download the mule-app-template using one of two ways:
    - Download the mule-app-template git repository;
    - Download the mule-app-template .jar from exchange and import using Anypoint Studio to unpack it.
- Modify the POM's node groupId to use the Business Group Id of your project
- In the POM modify the following tag

```
<distributionManagement>
  <repository>
    <id>anypoint-exchange-v3</id>
    <name>Corporate Repository</name>
    <url>https://maven.anypoint.mulesoft.com/api/v3/organizations/{Business Group Id}/maven</url>
    <layout>default</layout>
  </repository>
</distributionManagement>
```

- (option) If you have a Connected App: add the following XML tag to _.m2/settings.xml_

> Make sure your Connected App has the necessary permissions for the Business Group (Exchange Contributor and OpenID Profile).

```
<server>
  <id>anypoint-exchange-v3</id>
  <username>~~~Client~~~</username>
  <password>{Client ID}~?~{Client Secret}</password>
</server>
```

- (option) If you have a user: add the following XML tag to _.m2/settings.xml_

> Make sure your user has the necessary permissions for the Business Group (Exchange Contributor and OpenID Profile).
> Make sure your Anypoint Platform MFA is disabled or contact your admin to disable it.

```
<servers>
    <server>
      <id>anypoint-exchange-v3</id>
      <username>{username}</username>
      <password>{password}</password>
    </server>
  </servers>
```

- In the the mule-app-template directory run following command line

```
mvn clean deploy
```