deploy-elk
===========

Objective
---------

**This repo show how to deploy and configure elastic-serach, logstash and kibana easily using Ansible**

How to use it
=============

Variables
---------

* **elk_data_directory**: This is the root folder where elk data and configuration will be stored
* **elk_base_directory**: This is the base folder where elk data and configuration will be stored
* **elk_input_directory**: This is the folder where input files will be stored and used by logstash
* **elk_config_directory**: This is the folder where logtstash will be stored
* **elk_input_type**: This variable containt the `input type` used by logstash to classify and sort data (https://www.elastic.co/guide/en/logstash/current/plugins-inputs-file.html#plugins-inputs-file-type)
* **elk_input_type_2**: I've add the possibility to manage two `input type` (my use case), so feel free to use them or not

Playbook Description
--------------------

**deploy-and-configure.yml**: This is currently the main playbook
	* `create folders`
	* `copy configuration file`: input, filter and output files used by logstash to fully manage logs or your favorite files
	* `deploy container`: this is the most important part of the playbook, if you want more information about containerized elk you can read the folliwing documentation (https://elk-docker.readthedocs.io/)
	* `install plugins`: if you use some extra-plugin, there are a task to do that
	* `copy des patterns`: you can customize your logstash filter by using custom pattern define in a specific folder`

Example usage
-------------
`ansible-playbook -i hosts deploy-and-configure.yml`

Contribution
------------
You can contribute to this repository and share, i like sharing knowledge :-)

Author Information
------------------

- Dirane TAFEN (diranetafen@yahoo.com)

