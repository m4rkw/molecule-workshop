Molecule/TDD Workshop
=====================

1) Create your role directory with molecule:

````
$ molecule init --driver=docker --verifier=serverspec --role=apache
````

(replace apache with the name of your role)


2) Write serverspec tests in spec/default_spec.rb

Serverspec resource reference: http://serverspec.org/resource_types.html


3) Run the tests for your role to see them fail:

````
$ molecule test
````


4) Modify tasks/main.yml to implement the ansible code to make the tests pass.


Molecule steps
--------------

````
$ molecule create   - creates the VM/container
$ molecule destroy  - destroys the VM/container
$ molecule syntax   - verifies the ansible syntax
$ molecule converge - executes the ansible on the VM/container
$ molecule verify   - runs the serverspec tests on the VM/container
````


Tips
----

 * Run molecule converge repeatedly to re-run your ansible without destroying/recreating the container
 * Don't worry about configuring the various services - just get the main process running and tested


Workshop roles
--------------

easy:

- postfix - https://metapack.atlassian.net/browse/AWS-1116
- java8 - https://metapack.atlassian.net/browse/AWS-1117
- apache2.4 - https://metapack.atlassian.net/browse/AWS-1118
- ntp - https://metapack.atlassian.net/browse/AWS-1119
- nginx - https://metapack.atlassian.net/browse/AWS-1121

hard:

- python - https://metapack.atlassian.net/browse/AWS-1120
- filebeat - https://metapack.atlassian.net/browse/AWS-1122
- exim4 - https://metapack.atlassian.net/browse/AWS-1123
- dataloop-agent - https://metapack.atlassian.net/browse/AWS-1124
