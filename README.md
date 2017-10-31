# Ansible role `drupal`

An Ansible role for installing Drupal on RHEL/CentOS 7.

After applying this role, point your browser to http://SERVER_IP/drupal7/install.php and follow the instructions for configuring your site.

Remark that Drupal is installed from the package repository (EPEL), not from the Drupal project itself. If you need a role that gives you full control over Drupal, PHP versions, drush, etc., take a look at Jeff Geerling's role ([geerlingguy.drupal](https://galaxy.ansible.com/geerlingguy/drupal/)).

## Requirements

No specific requirements

## Role Variables


| Variable               | Default     | Comments (type)                             |
| :---                   | :---        | :---                                        |
| `drupal_database`      | 'drupal'    | Name of the database Drupal can make use of |
| `drupal_username`      | 'drupal'    | Database user for Drupal                    |
| `drupal_password`      | 'drupal'    | Password for the database user.             |
| `drupal_database_host` | 'localhost' | Database server                             |
| `drupal_prefix`        | ''          | Prefix value for table names                |

## Dependencies

- [bertvv.httpd](https://galaxy.ansible.com/bertvv/httpd/)

## Example Playbook

See the test playbooks in either the [Vagrant](https://github.com/bertvv/ansible-role-drupal/blob/vagrant-tests/test.yml) or [Docker](https://github.com/bertvv/ansible-role-drupal/blob/docker-tests/test.yml) test environment. See the section Testing for details.

## Testing

There are two types of test environments available. One powered by Vagrant, another by Docker (TODO). The latter is suitable for running automated tests on Travis-CI. Test code is kept in separate orphan branches. For details of how to set up these test environments on your own machine, see the README files in the respective branches:

- Vagrant: [vagrant-tests](https://github.com/bertvv/ansible-role-drupal/tree/vagrant-tests)
- Docker: [docker-tests](https://github.com/bertvv/ansible-role-drupal/tree/docker-tests)

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch.

## License

2-clause BSD license, see [LICENSE.md](LICENSE.md)

## Contributors

- [Bert Van Vreckem](https://github.com/bertvv/) (maintainer)

