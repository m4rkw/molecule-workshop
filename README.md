Molecule/TDD Workshop
=====================

Instructions
------------


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
