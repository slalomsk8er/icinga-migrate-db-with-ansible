# Migrate Icinga2 and Icingaweb2 Databases with Ansible
A quick and dirty (not idempotent) ansible-playbook to migrate databases form master to a MariaDB cluster.

Be carfull as there could be bugs. The playbook was growing while I migrated the DBs - no modules DB migration was done after I started work on the IDO-DB part!

## Usage hints

 * Use `--chec` and `-vvv` for testing.
 * use `--extra-vars` to overload variables.
 * use vault for passwords
 
 
    `ansible-playbook mv_db_to_cluster.yml --check --ask-vault-pass --extra-vars '{ "icinga_mv_db_module_name": "", "icinga_mv_db_resource_name": "icinga_ido"}' `
