# Open Distro For Elasticsearch Security Parent

Open Distro for Elasticsearch Security Parent is the parent repo for the Open Distro for Elasticsearch security plugin repositories, including:

[Security]( https://github.com/opendistro-for-elasticsearch/security)

[Security-SSL]( https://github.com/opendistro-for-elasticsearch/security-ssl)

[Security Advanced Modules]( https://github.com/opendistro-for-elasticsearch/security-advanced-modules)

[Security Kibana Plugin]( https://github.com/opendistro-for-elasticsearch/security-kibana-plugin)

## Documentation
Please refer to the [technical documentation](https://opendistro.github.io/for-elasticsearch-docs) for detailed information.

## Requirements

Make sure you are in the elasticsearch/linux_distributions folder. Here are the instructions for installing Java (OpenJDK 11) for Debian based distributions.

```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt install openjdk-11-jdk
```

## Build
To build the security plugin from source follow these instructions **in this order**:


1. Download the `security-parent` source code:

`git clone https://github.com/opendistro-for-elasticsearch/security-parent.git`

`cd security-parent`


2. Install to the local repository folder named `.m2`: 

`mvn clean install`

`cd ..`

3. Download the `security` source code:

`git clone https://github.com/opendistro-for-elasticsearch/security.git`

`cd security`

4. Install to the local repository folder named `.m2`: 

`mvn clean install`

`cd ..`

5. Download the `security-ssl` source code: 

**(Note: This step works only for plug-in versions below 1.0.0.0 [ Elasticsearch 7.0.1 ])**

`git clone https://github.com/opendistro-for-elasticsearch/security-ssl.git`

`cd security-ssl`

6. Install to the local repository folder named `.m2`: 

`mvn clean install`

`cd .. `

7. Download the `security-advanced-modules` source code:

`git clone https://github.com/opendistro-for-elasticsearch/security-advanced-modules.git`

`cd security-advanced-modules`

8. Install to the local repository folder named `.m2`: 

`mvn clean install`

`cd .. `

9. Build the Elasticsearch plugin:

`cd security`

10. Install final artifacts:

`mvn clean package -Padvanced` 

The above builds the final artifacts in zip format. 

`cd target/releases/`

The artifacts can be found in the folder listed above.

11. Detailed instructions on how to build the **security-kibana** plugin can be found here: 

https://github.com/opendistro-for-elasticsearch/security-kibana-plugin/blob/master/README.md#build


## Install

Install the plugin to your Elasticsearch cluster with the following commands:

`cd elasticsearch/bin`


`./elasticsearch-plugin install file:///path/to/security/target/releases/opendistro_security-<version>.zip`


## License

This code is licensed under the Apache 2.0 License. 

## Copyright

Open Distro For Elasticsearch Security Copyright 2019 Amazon.com, Inc. or its affiliates. All Rights Reserved.

