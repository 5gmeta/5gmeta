### Hey, this is 5GMETA! 👋

<!--
**5gmeta/5gmeta** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

![5GMETA logo.](./5GMETA_logo.png)
### 🍿 Introduction to the 5GMETA Platform
5GMETA is an open data-centric Internet of Things (IoT) messaging platform for Connected and Automated Mobility (CAM) applications and service providers. The 5GMETA Platform creates a CAM data monetization ecosystem that allows different stakeholders along the data value chain to exploit data in a more effective and profitable way.​

A fundamental principle supported by the 5GMETA Platform is that of achieving a total decoupling between Data Producers and Data Consumers. This means that Data Producers do not need to be directly connected to Data Consumers. The 5GMETA Platform acts as a broker between Data Producers (vehicles or RSUs) and Data consumers (third-party applications or services). However, the 5GMETA Platform is not a simple publish-subscribe broker, and it includes functions for data management, data monetization and cybersecurity as well as providing data access mechanisms. In contrast with a Data Lake, the 5GMETA Platform provides live data delivery. The users of the 5GMETA Platform receive the data from the subscribed dataflows in a continuous manner with no storage service within the 5GMETA Platform rather than the required memory buffering. 

These two videos are a good starting point to learn more about the motivation and the basic concepts of the 5GMETA Platform:
* Video 1: [The 5GMETA Project](https://youtu.be/keB3PlQNiec?si=Cq94v0SMFuGyYSBp)
* Video 2: [The 5GMETA Platform](https://youtu.be/RGVD8D0ZwQc?si=t2R2ufpkzkGtogDm)

The Road to Lisbon hackathon webinars are also a great resource:
* [Road to Lisbon_5GMETA Hackathon Webinar #1_Introduction to the Platform](https://youtu.be/-ph7cs_wQa0?si=o6LmF-CHhLxCayTw)
* [Road to Lisbon 5GMETA Hackathon Webinar #2 How to interface with the platform](https://youtu.be/5iSsRsp_II4?si=QglJpST5SNm0loHj)
* [Road to Lisbon 5GMETA Hackathon Webinar #3 Choosing and using available data](https://youtu.be/6Z026lECwlQ?si=WlPHvQyRh5YDnDnO)

More info can also be found on the [5GMETA website](https://5gmeta-project.eu/).

### ⚡ 5GMETA Platform components
<!-- table with components, link and one sentence describing component -->

| Repository          | Description                                                                                                                                                                                                                                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [5gmeta-dev](https://github.com/5gmeta/5gmeta-dev)         | Contains the documentation, examples and tutorials related to the 5GMETA platform.                                                                                                                                                                                                                                                     |
| [cloud_instanceapi](https://github.com/5gmeta/cloud_instanceapi)   | This API is the central access point to request to the different MECs that are part of the platform to deploy instances on them depending on instancetype and datatype.                                                                                                                                                                |
| [dashboard](https://github.com/5gmeta/dashboard)           | The main objective of the dashboard is to provide a graphical interface to the data consumers allowing them to benefit from the 5GMETA platform features that are otherwise only accessible using API requests.                                                                                                                        |
| [data_quality](https://github.com/5gmeta/data_quality)        | Contains the data quality assessment module based on ETSI TS 103 759 V2.1.1 (2023-01). This module assigns to each dataflow a quality value from 1 to 7.                                                                                                                                                                               |
| [dataflow-api](https://github.com/5gmeta/dataflow-api)        | Contains all the components needed to implement a Flask webserver providing the Dataflow APIs to a third party application.                                                                                                                                                                                                            |
| [dataflow_cloud](https://github.com/5gmeta/dataflow_cloud)      | Related to the dataflow database Cloud building block of the 5GMETA Platform, and to be deployed at the 5GMETA Cloud level for storing the metadata (commonly named dataflow in the project) related to producted & consumed data.                                                                                                     |
| [discovery](https://github.com/5gmeta/discovery)           | This API is in charge of managing all neccessary information about MECs and their capabilities, coverage zones (tiles) and services provided by them to 3rd party applications and to 5GMETA platform members.                                                                                                                         |
| [helmcharts](https://github.com/5gmeta/helmcharts)          | Includes the HELM charts required by K8s to deploy platform systems at Cloud and MEC and to instantiate data pipelines in a specific MEC triggered by a request from a data consumer.                                                                                                                                                  |
| [identity](https://github.com/5gmeta/identity)            | Hosts the code and the resources regarding the Identity module: the identity manager based on Keycloak and the user information manager based on Spring Boot.                                                                                                                                                                          |
| [license](https://github.com/5gmeta/license)             | Hosts the source code for the license API of the 5GMETA platform. For the platform operator, the license API allows the management of the dataflow licenses to be made available to the data consumers i.e. creation, update and deletion. For the data consumers, the license API allows to retrieve the available dataflow licenses. |
| [llccam](https://github.com/5gmeta/llccam)              | Shows how to deploy a CCAM Application in the MEC Platform of 5GMETA (using 5GMETA HW resources instead of deploying it in the Third-Party premises).                                                                                                                                                                                  |
| [message-data-broker](https://github.com/5gmeta/message-data-broker) | Contains an ActiveMQ message broker to be deployed in the MEC.                                                                                                                                                                                                                                                                         |
| [metering](https://github.com/5gmeta/metering)            | Contains the documentation and resources to deploy the monitoring tools to meter the computer usage and the data consumption volume. This information could be used to charge users in a pay-as-you go pricing aproach.                                                                                                                |
| [orchestrator](https://github.com/5gmeta/orchestrator)        | Contains all the components necessary to get a working Edge Stack where the pipelines requested from a third-party will be deployed to handle specific data-types.                                                                                                                                                                     |
| [platform-config](https://github.com/5gmeta/platform-config)     | Includes all the guidelines to deploy both, the MEC and the Cloud systems of the 5GMETA platform.                                                                                                                                                                                                                                      |
| [registration](https://github.com/5gmeta/registration)        | Contains all the components needed to implement the Registration API, a Flask webserver running on the Edge, providing REST APIs to interact with a dataflow database.                                                                                                                                                                 |
| [stream-data-gateway](https://github.com/5gmeta/stream-data-gateway) | Contains all the components and connectors necessary to retrieve data from MEC data pipelines and make them accessible to consumers in internet through the 5GMETA Cloud platform.                                                                                                                                                     |
| [video-anonymizator](https://github.com/5gmeta/video-anonymizator)  | Contains all necessary stuff to build video and image anonimizator modules for 5GMETA platform.                                                                                                                                                                                                                                        |
| [video-stream-broker](https://github.com/5gmeta/video-stream-broker) | Provides the modules to push a video stream to the MEC infrastructure and how the Broker performs the signalling and the streaming of Video flows in a standard way.                                                                                                                                                                   |
| [vnfdescriptors](https://github.com/5gmeta/vnfdescriptors)      | Includes the VNF descriptors required by OSM to instantiate data pipelines in a specific MEC triggered by a request from a data consumer                                                                                                                                                                                               |

### :raising_hand: Contributing to the platform

Contributions are welcome :blush: See [how to contribute](./CONTRIBUTING.md).

