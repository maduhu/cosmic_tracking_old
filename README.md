# Cosmic
Cosmic is open source software designed to deploy and manage large
networks of virtual machines, as a highly available, highly scalable
Infrastructure as a Service (IaaS) cloud computing platform. Cosmic
provides an on-premises (private) cloud offering, or as part of a
hybrid cloud solution.

Cosmic is a turnkey solution that includes the entire "stack" of features
most organizations want with an IaaS cloud: compute orchestration,
Network-as-a-Service, user and account management, a full and open native API,
resource accounting, and a first-class User Interface (UI).

Cosmic currently supports the most popular hypervisors:
VMware vSphere, KVM, XenServer, XenProject and Hyper-V as well as
OVM and LXC containers.

Users can manage their cloud with an easy to use Web interface, command line
tools, and/or a full-featured query based API.

## Getting Source Repository

Cosmic officials Git repository is located at:

    https://github.com/missioncriticalcloud/cosmic

## Building from Source

In order to build Cosmic, you have to follow the steps below:

* For KVM
  1. git clone --recursive git@github.com:MissionCriticalCloud/cosmic.git
  2. cd cosmic
  3. mvn clean install -P developer,systemvm

- Don't have a developer key yet? Please contact us! [Email](int-cloud@schubergphilis.com)

The steps above will build the essencials to get Cosmic management server working. Besides that, you will also need a hypervisor. That can be discussed another time. for now, in order to see something working, please do:

1. cd cosmic-client
2. mvn -pl :cloud-client-ui jetty:run

Go to your brouwser and type: http://localhost:8080/client

## Links

Cosmic is a fork of Apache CloudStack and it is backwards compatible with CloudStack's API. So, all the documentation can be accessed from:

* [Documentation](http://docs.cloudstack.apache.org)
* API [documentation](http://cloudstack.apache.org/docs/api)

## Getting Involved

Please, join our Slack channel for more details:

* [Mission Critical Cloud](https://missioncriticalcloud.slack.com)

## Reporting Security Vulnerabilities

If you've found an issue that you believe is a security vulnerability in a
released version of Cosmic, please report it to `int-cloud@schubergphilis.com` with details about the vulnerability, how it
might be exploited, and any additional information that might be useful.

## License

Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.

Please see the [LICENSE](LICENSE) file included in the root directory
of the source tree for extended license details.

## Notice of Cryptographic Software

This distribution includes cryptographic software. The country in which you currently
reside may have restrictions on the import, possession, use, and/or re-export to another
country, of encryption software. BEFORE using any encryption software, please check your
country's laws, regulations and policies concerning the import, possession, or use, and
re-export of encryption software, to see if this is permitted. See http://www.wassenaar.org/
for more information.

The U.S. Government Department of Commerce, Bureau of Industry and Security (BIS), has
classified this software as Export Commodity Control Number (ECCN) 5D002.C.1, which
includes information security software using or performing cryptographic functions with
asymmetric algorithms. The form and manner of this Apache Software Foundation distribution
makes it eligible for export under the License Exception ENC Technology Software
Unrestricted (TSU) exception (see the BIS Export Administration Regulations, Section
740.13) for both object code and source code.

The following provides more details on the included cryptographic software:

* Cosmic makes use of JaSypt cryptographic libraries
* Cosmic has a system requirement of MySQL, and uses native database encryption functionality.
* Cosmic makes use of the Bouncy Castle general-purpose encryption library.
* Cosmic can optionally interacts with and controls OpenSwan-based VPNs.
* Cosmic has a dependency on and makes use of JSch - a java SSH2 implementation.
