# Open Distro For Elasticsearch Security Parent

Open Distro for Elasticsearch Security Parent is a parent repo for the Open Distro for Elasticsearch Security related repositories, including:

[Security]( https://github.com/opendistro-for-elasticsearch/security)

[Security-SSL]( https://github.com/opendistro-for-elasticsearch/security-ssl)

[Security Advanced Modules]( https://github.com/opendistro-for-elasticsearch/security-advanced-modules)

[Security Kibana Plugin]( https://github.com/opendistro-for-elasticsearch/security-kibana-plugin)

## Documentation
Please refer to the [technical documentation](https://opendistro.github.io/for-elasticsearch-docs) for detailed information.

## Build
To build the security plugin from source follow these instructions **in this order**:


Download the `security-parent` source code

`git clone https://github.com/opendistro-for-elasticsearch/security-parent.git`

`cd security-parent`


Install to the .m2 directory: 


`mvn clean install`

`cd ..`

Download the `security` source code

`git clone https://github.com/opendistro-for-elasticsearch/security.git`

`cd security`

Install to the `.m2` directory: 


`mvn clean install`

`cd ..`

Download the `security-ssl` source code **(only for versions < 1.0.0.0 [ Elasticsearch 7 ])**

`git clone https://github.com/opendistro-for-elasticsearch/security-ssl.git`

Install to the `.m2` directory: 


`cd security-ssl`

`mvn clean install`

`cd .. `


Download the `security-advanced-modules` source code

`git clone https://github.com/opendistro-for-elasticsearch/security-advanced-modules.git`

Install to the `.m2` directory: 


`cd security-advanced-modules`

`mvn clean install`

`cd .. `

Build the Elasticsearch plugin

`cd security`

`mvn clean package -Padvanced` This builds the final artifacts in zip format. 

`cd target/releases/`



## Install

Install the plugin to your Elasticsearch cluster with the following commands:

`cd elasticsearch/bin`


`./elasticsearch-plugin install file:///path/to/security/target/releases/opendistro_security-<version>.zip`


## License

This code is licensed under the Apache 2.0 License. 

## Copyright

Open Distro For Elasticsearch Security Copyright 2019 Amazon.com, Inc. or its affiliates. All Rights Reserved.

