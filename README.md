marathon-lb Role
=========

Configure and run marathon-lb in a docker container using the image `mesosphere/marathon-lb`

This role has been specifically developed to be used for the deployment of Mesos/Marathon in the framework of INDIGO-DataCloud project.

Role Variables
--------------

- `marathon_lb_marathon_url`: Marathon endpoint (default: "http://marathon.service.consul:8080")
- `marathon_lb_ports`: haproxy bind port (default: 9090)
- `marathon_lb_auth_creds`: user/pass for the Marathon HTTP API in the format of 'user:pass'
- `marathon_lb_group`: Only generate config for apps which list the specified names (default: external)


Dependencies
------------

- `indigo-dc.docker`

Example Playbook
----------------

This is an example of how to use `marathon-lb` role:

    - hosts: servers
      roles:
         - { role: indigo-dc.marathon-lb, marathon_lb_auth_creds: "admin:s3cret" }


License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0


Author information
------------------

Marica Antonacci
marica.antonacci@ba.infn.it,
marica.antonacci@gmail.com

