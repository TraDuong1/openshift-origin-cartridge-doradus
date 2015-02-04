# OpenShift Doradus Cartridge

The `doradus` cartridge provides [Doradus](https://github.com/dell-oss/Doradus) on OpenShift.

The downloadable URL is : https://raw.githubusercontent.com/TraDuong1/openshift-origin-cartridge-doradus/master/metadata/manifest.yml

* Do not forget to set Cartridge environment variable for Doradus which contain all the connection info of the Cassandra cluster/node.

  rhc env set CASSANDRA_NODE_IP=<CASSANDRA_NODE_IP> CASSANDRA_NODE_PORT=<CASSANDRA_NODE_PORT> CASSANDRA_SUPERUSER_NAME=<CASSANDRA_SUPERUSER_NAME> CASSANDRA_SUPERUSER_PW=<CASSANDRA_SUPERUSER_PW>

* Then simply use with 'rhc' client tools to add cartridge
  rhc cartridge add https://raw.githubusercontent.com/TraDuong1/openshift-origin-cartridge-doradus/master/metadata/manifest.yml —app <app_name>


## Environment Variables

The `doradus` cartridge provides several environment variables to reference for ease
of use:

    OPENSHIFT_DORADUS_HOST      The Doradus IP address
    OPENSHIFT_DORADUS_PORT      The Doradus port
    OPENSHIFT_DORADUS_LOG_DIR   The path to the Doradus log directory

For more information about environment variables, consult the
[OpenShift Application Author Guide](https://github.com/openshift/origin-server/blob/master/node/README.writing_applications.md).
