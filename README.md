# Cloudera Director Configs
Sample config files for creating CDH clusters using Cloudera Director

## Steps
1. Install Cloudera Director according to [documentation](https://www.cloudera.com/documentation/director/latest/topics/director_get_started.html)
2. Edit the config file that you're interested in. Descriptions below:
 * aws_simple.conf - Simple config with Spark 2, Impala, Kudu, Java 8
 * aws_kb.conf - Kerberized cluster (need an existing KDC setup before-hand)
 * aws_kb_tls.conf - Kerberized and TLS-enabled cluster (using Director autoTLS)
3. Copy AWS private key to ```director_configs/kp.pem```
4. Edit AWS credentials and source them to environment variables: ```source director_configs/creds.sh```
5. Run Cloudera Director: ```cloudera-director bootstrap director_configs/aws_simple.conf```
