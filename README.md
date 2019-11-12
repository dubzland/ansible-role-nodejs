# Dubzland: Node.js
[![Gitlab pipeline status (self-hosted)](https://img.shields.io/gitlab/pipeline/jdubz/dubzland-nodejs?gitlab_url=https%3A%2F%2Fgit.dubzland.net)](https://git.dubzland.net/jdubz/dubzland-nodejs/pipelines)

Installs and configures Node.js and Yarn from source.

## Requirements

Ansible 2.2 or higher.

## Role Variables

Available variables are listed below, along with their default values (see
    `defaults/main.yml` for more info):

### dubzland_nodejs_version

```yaml
dubzland_nodejs_version: "12.13.0"
```

Specific version of Node.js to install.

### dubzland_nodejs_source_root

```yaml
dubzland_nodejs_source_root: "/usr/local/src"
```

Directory used to store tarballs, as well as extract and build source tree.

### dubzland_nodejs_source_url

```yaml
dubzland_nodejs_source_url: "https://nodejs.org/dist/v12.13.0/node-v12.13.0.tar.gz"
```

URL used to download Node.js source tarball.

### dubzland_nodejs_source_sha256sum

```yaml
dubzland_nodejs_source_sha256sum: "2e5321e095fe673a3ab936cf77faf8c983cba62f27a9fbd00530a7edb739a040"
```

SHA256 checksum used to validate the downloaded source tarball.

### dubzland_nodejs_build_jobs

```yaml
dubzland_nodejs_build_jobs: 4
```

Number of parallel make jobs to execute.

### dubzland_nodejs_yarn_key_url

```yaml
dubzland_nodejs_yarn_key_url: "https://dl.yarnpkg.com/debian/pubkey.gpg"
```

Url used to download the GPG key for the Yarn repository.

### dubzland_nodejs_yarn_repo_url

```yaml
dubzland_nodejs_yarn_repo_url: "deb https://dl.yarnpkg.com/debian/ stable main"
```

Url added to package cache for the Yarn repository.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: dubzland-nodejs
```

## License

MIT

## Author

* [Josh Williams](https://codingprime.com)
