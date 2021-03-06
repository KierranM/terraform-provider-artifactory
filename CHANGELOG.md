## 1.5.0
DEPRECATIONS:
* The `token` provider attribute has been deprecated. It has been renamed to
  `api_key` to distinguish it from the new `access_token` parameter.
* `artifactory_permission_targets` resource has been deprecated in favour of the new
  v2 API in 6.6+. The new v2 resource has been named `artifactory_permission_target`
  The old v1 permission target will be supported until the EOL of artifactory 6.5.x

FEATURES:
* Add build action permission support [#21]
* Support supplying user passwords with special characters [#27] 
 
BUG FIXES
* Add xray_index field to local and remote repos [#26]
* Add bower fields to remote repos [#29]

Notes:
* Bumped to terrafom v0.11.13

## 1.4.3 (January 22, 2019)
BUG FIXES:
* Fixed setting of passwords in replications and remote repository

NOTES:
* Added integration tests
* Bumped to terraform v0.11.11
* Cleaned up lint checks and build

## 1.4.2 (December 4, 2018)
FEATURES:
* Added docs website [#14]

BUG FIXES:
* Added enable_token_authentication to remote repositories [#18]

## 1.4.1 (November 6, 2018)
BREAKING CHANGES:
* Removed makefile and githooks in favour of default go tool commands.

FEATURES:
* Add support for supplying user password on creation via the environment variable:
  
  ```TF_USER_${artifactory_username_here}_PASSWORD```
    
  This variable may change and is not tracked by terraform

NOTES:
* Removed formatting checks from CI and streamlined build.
* Migrate from dep to go modules. This is transparent for consumers but requires go 1.11+ for development.
