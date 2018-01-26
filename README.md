	To setup kafka cluster on aws via ansible.
Requirement: IP detail of Zookeeper Cluster
	There are two ways to get the IP detail of Zookeeper cluster either static or get it through dynamic inventory by using a variable.
zookeeper_group is variable which will look for hosts from dynamic inventory.


	If you want to mount an additional partition for kafka then define kfebs_vol and update the variable kafka_data_dir accordingly
	e.g
		kfebs_vol:
	          - partition: /dev/sdb
                    mountpoint:/mnt


	Notes: All the variables are defined in default/main.yml which are having low priority so you can overwrite it by defining either vars/main.yml or group_vars
