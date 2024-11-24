## [1.3.0](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.2.1...1.3.0) (2024-11-24)

### Features

* created role to set hostname ([12b8354](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/12b8354e7a3bb95584f00518d7e80bf2d2966d8a))

## [1.2.1](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.2.0...1.2.1) (2024-11-23)

### Bug Fixes

* updated nexus URLs for debian ([857a3aa](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/857a3aae88a3aab580676e3950f8b20c51d0e6c3))

## [1.2.0](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.7...1.2.0) (2024-11-20)

### Features

* created role to setup pip to use nexus pypi mirror ([40718be](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/40718be0d22fb74de216e0b05a5546f742eef5dd))

## [1.1.7](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.6...1.1.7) (2024-11-17)

### Bug Fixes

* added remote sourc to apt_nexus_mirror copy modules ([70997ef](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/70997ef7252ba3eb70106c662fe12ab9b0c78b58))

## [1.1.6](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.5...1.1.6) (2024-11-16)

### Bug Fixes

* removed lingering handler ref ([005d8a5](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/005d8a5a5efb79d4753dd838b5c7820a5aa4773e))

## [1.1.5](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.4...1.1.5) (2024-11-16)

### Bug Fixes

* moved apt update to task from handler ([2184ca3](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/2184ca3a27ed3a383f164fe16e9b59d65131a0bb))

## [1.1.4](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.3...1.1.4) (2024-11-16)

### Bug Fixes

* added step for Debian to clear debian.sources ([1acb944](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/1acb944b79f51e5a7767b5a130314af4c7d1ca6b))

## [1.1.3](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.2...1.1.3) (2024-11-16)

### Bug Fixes

* updated nexus_sources var name ([efc5b66](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/efc5b66df3866f49832dff1cfec23b31a337abe6))

## [1.1.2](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.1...1.1.2) (2024-11-16)

### Bug Fixes

* renamed task to tasks in apt_nexus_Mirror ([92d5aa8](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/92d5aa81372289e15900ee41768ae121e7a2ceba))

## [1.1.1](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.1.0...1.1.1) (2024-11-16)

### Bug Fixes

* moved vars to defaults ([bc41bb6](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/bc41bb65efbfdc67944c2b139a61d5ed9eb20a30))

## [1.1.0](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/1.0.0...1.1.0) (2024-11-16)

### Features

* made role to setup apt nexus mirrors ([ba8ba04](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/ba8ba04b669d97778c130bfe9025abb6d05e1c98))

## [1.0.0](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/compare/...1.0.0) (2024-11-05)

### Bug Fixes

* added galaxy file to make it into a collection ([e9ccb89](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/e9ccb899a8ea17909572958977f9323043d3eabb))
* added meta file for dockerhub_nexus_mirror ([dbd4c48](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/dbd4c4870eef92484bbd043fd869fd48b29d6798))
* made husky ansible-lint only scan roles dir ([23fd485](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/23fd485457200b7a5e63587df187b17b7016df49))

### Features

* added ansible-dev-tools to devcontainer ([bc3a883](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/bc3a883cc9e88df09590ecd5e8751467516846d5))
* added devcontainer to project ([7279eea](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/7279eeaec80432f2d5f6df0d42eba0f6537c6ca5))
* added disable_user role ([2a6f09f](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/2a6f09fb13e8ff26254c205497e4299129037b43))
* added husky git hooks to project ([626a745](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/626a745f6cf81b9eebf742d6e7f2eb31f1f5a389))
* added semantic-release GHA to project ([ab46aef](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/ab46aef4ab829d138567aa7b18e53dbdc8e83651))
* created dockerhub_nexus_mirror role ([fffa32a](https://github.com/Johnny-Knighten/ansible-homelab-common-roles/commit/fffa32af12d59c9d1ae6245bb711e156d8e7b0a2))
