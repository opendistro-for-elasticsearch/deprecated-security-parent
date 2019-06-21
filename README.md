# Open Distro For Elasticsearch Security Parent

Open Distro for Elasticsearch Security Parent is a parent repo for the Open Distro for Elasticsearch Security related repositories, including:

[Security]( https://github.com/opendistro-for-elasticsearch/security)

[Security-SSL]( https://github.com/opendistro-for-elasticsearch/security-ssl)

[Security Advanced Modules]( https://github.com/opendistro-for-elasticsearch/security-advanced-modules)

[Security Kibana Plugin]( https://github.com/opendistro-for-elasticsearch/security-kibana-plugin)

## Documentation
Please refer to the [technical documentation](https://opendistro.github.io/for-elasticsearch-docs) for detailed information.

## Build
To build the security plugin from source follow these instructions:



Download the `security-parent` source code

`git clone https://github.com/opendistro-for-elasticsearch/security-parent.git`

`cd security-parent`

`mvn clean install`

`cd ..`

Download the `security` source code

`git clone https://github.com/opendistro-for-elasticsearch/security.git`

`cd security-parent`

`mvn clean install`

`cd ..`

Download the `security-advanced-modules` source code

`git clone https://github.com/opendistro-for-elasticsearch/security-advanced-modules.git`

`cd security-parent`

`mvn clean install`

`cd .. `

Build the plugin

`cd security`

`mvn clean package -DskipTests -Padvanced`

`cd target/releases/`


## License

This code is licensed under the Apache 2.0 License. 

## Copyright

Open Distro For Elasticsearch Security Copyright 2019 Amazon.com, Inc. or its affiliates. All Rights Reserved.

