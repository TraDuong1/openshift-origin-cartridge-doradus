# OpenShift Doradus Cartridge

The `doradus` cartridge provides [Doradus](https://github.com/dell-oss/Doradus) on OpenShift.

The downloadable URL is : https://raw.githubusercontent.com/TraDuong1/openshift-origin-cartridge-doradus/master/metadata/manifest.yml

It is required to tell Doradus where the Cassandra cluster/node can be reached by setting Cartridge environment variables below.

    rhc env set CASSANDRA_NODE_IP=<CASSANDRA_NODE_IP> CASSANDRA_NODE_PORT=<CASSANDRA_NODE_PORT> CASSANDRA_SUPERUSER_NAME=<CASSANDRA_SUPERUSER_NAME> CASSANDRA_SUPERUSER_PW=<CASSANDRA_SUPERUSER_PW>

To deploy this cartridge, you simply provide the URL of the cartridge manifest from the CLI or admin console. OpenShift will then download and install the cartridge for you.

    rhc cartridge add https://raw.githubusercontent.com/TraDuong1/openshift-origin-cartridge-doradus/master/metadata/manifest.yml —app <app_name>

Other useful cartridge management commands

    rhc cartridge status <cartridge_name>

    rhc cartridge start <cartridge_name>

    rhc cartridge stop  <cartridge_name>

## Environment Variables

The `doradus` cartridge provides several environment variables to reference for ease
of use:

    OPENSHIFT_DORADUS_HOST      The Doradus IP address
    OPENSHIFT_DORADUS_PORT      The Doradus port
    OPENSHIFT_DORADUS_LOG_DIR   The path to the Doradus log directory

For more information about environment variables, consult the
[OpenShift Application Author Guide](https://github.com/openshift/origin-server/blob/master/node/README.writing_applications.md).
