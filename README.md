## OpenShift filebeat Cartridge

This is a simple cartridge for making filebeat easily available in your applications.


## Environment Variables

These environment variables are used when configuring Filebeat:

 * **`OPENSHIFT_FILEBEAT_LOGSTASH_HOST`**: URL of the logstash host to log to. Required.
 * **`OPENSHIFT_FILEBEAT_LOGSTASH_PORT`**: Port logstash is running on. Required.
 * **`OPENSHIFT_FILEBEAT_LOGSTASH_TLS`**: Configure logstash to use TLS. Optional.
 * **`OPENSHIFT_FILEBEAT_LOGSTASH_TLS_CA_FILENAME`**: CA certificate filename. (path from home) Optional. e.g. app-root/repo/resources/logstash_ca.crt

## Installation

First, configure the application with the appropriate environment variables. Then, add the cartridge to your application:

    # Configure environment
    $ rhc set-env --app my-app --env "OPENSHIFT_FILEBEAT_LOGSTASH_HOST=abc123-us-east-1.foundcluster.com"
    $ rhc set-env --app my-app --env "OPENSHIFT_FILEBEAT_LOGSTASH_PORT=XXXX"

    # Add cartridge
    $ rhc cartridge add -a your-app-name https://cartreflect-claytondev.rhcloud.com/github/acrollet/openshift-cartridge-filebeat

## License

Released under the [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0.html).
