Summary
=======

This template assists developers in creating Mule applications more efficiently while maintaining consistent naming conventions and improving overall quality.

What is this?
=======

## Mule files

![resources/image-2023-10-16_16-4-5.png](resources/image-2023-10-16_16-4-5.png)

 - The global file keeps all the global elements of the applications (e.g. HTTP Connector)

![resources/image-2023-10-16_16-4-30.png](resources/image-2023-10-16_16-4-30.png)

 - The interface file keeps the code for the basic configuration settings for the API, such as the base path, version, and endpoint details.

![resources/image-2023-10-16_16-4-52.png](resources/image-2023-10-16_16-4-52.png)

 - TO_DELETE is file to keep global properties that are for local use only, (e.g. secure-key) and as the name indicates it to be  deleted before deployment to cloudhub

![resources/image-2023-10-16_16-5-9.png](resources/image-2023-10-16_16-5-9.png)

 - The Resource is where the logic of the API resided, like call to  other API's, choice flows..., this file should be named after the resource it manipulates (e.g. accounts) and a new should be created for each one

![resources/image-2023-10-16_16-5-32.png](resources/image-2023-10-16_16-5-32.png)

## Resource files

![resources/image-2023-10-16_16-6-23.png](resources/image-2023-10-16_16-6-23.png)

 - The Secure Properties folder holds the   secure properties files separated by environments

![resources/image-2023-10-16_16-7-20.png](resources/image-2023-10-16_16-7-20.png)

 - In the resource folder the re is a pre-made keystore (keystore-example.jks) it can be replaced with one that applies to your specific scenario

![resources/image-2023-10-13_16-34-13.png](resources/image-2023-10-13_16-34-13.png)

 - The Properties folder holds the properties files separated by environments, a file for common properties not depend on the environment and a error-properties file

![resources/image-2023-10-16_16-8-50.png](resources/image-2023-10-16_16-8-50.png)

![resources/image-2023-10-16_16-9-30.png](resources/image-2023-10-16_16-9-30.png)

![resources/image-2023-10-16_16-10-2.png](resources/image-2023-10-16_16-10-2.png)