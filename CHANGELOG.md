# Change Log

All notable changes to this project will be documented in this file.

## [Unreleased][unreleased]

## [v0.0.6] - 2016-01-06
### Added
- `AWS.DirectoryService` module has new functionality for managing and
  verifying trust relationships.
- `AWS.Client` has new `proto` and `port` members that can be used to create a
  client that is suitable for use with Local DynamoDB.  In this situation, the
  region should be set to `local`, the protocol to `http` and the port should
  match the running Local DynamoDB instance.
- `AWS.ECS` has updated documentation.
- `AWS.Logs` has updated documentation.
- `AWS.SSM` has updated documentation.

### Changed
- Services return an `{:ok, nil, response}` 3-tuple, instead of the `{:ok,
  response}` 2-tuple that was previously returned, when an AWS service
  endpoint returns a successful HTTP status with an empty response body.
- Relax `Poison` dependency to 1.2.0 to maintain compatibility with
  [ex_aws](https://hex.pm/packages/ex_aws).

## [v0.0.5] - 2015-11-06
### Changed
- All services return a `{:error, reason, response}` tuple when an
  unsuccessful HTTP status code is returned (previously the `response` was not
  included).

### Fixed
- An empty body returned alongside an HTTP 200 from an AWS service isn't
  parsed by Poison (which was causing exceptions to be raised).  Thanks Mike
  Coleman aka @fivebats.

## [v0.0.4] - 2015-08-05
### Added
- `AWS.CloudSearch.Domain` module for Cloud Search Service.
- `AWS.Cognito.Sync` module for Cognito Sync Service.
- `AWS.DeviceFarm` module for DeviceFarm Service.
- `AWS.EFS` module for Elastic File System Service.
- `AWS.Glacier` module for Glacier Service.
- `AWS.Lambda` module for Lambda Service.
- `AWS.MobileAnalytics` module for Mobile Analytics Service.
- `AWS.Transcoder` module for Elastic Transcoder Service.

### Changed
- `AWS.CloudHSM` module has updated documentation.
- `AWS.CognitoIdentity` module has been renamed to `AWS.Cognito`.
- `AWS.Logs` module has support for new `DeleteDestination`,
  `DescribeDestinations`, `PutDestination` and `PutDestinationPolicy` actions.
- `AWS.OpsWorks` module has updated documentation and new support for the
  `DeregisterEcsCluster`, `DescribeEcsClusters` and `RegisterEcsCluster`
  actions.
- `AWS.Route53Domains` module has been renamed to `AWS.Route53.Domains`.
- `AWS.StorageGateway` module has updated documentation.

## [v0.0.3] - 2015-07-14
### Added
- `AWS.DynamoDB.Streams` module for DynamoDB Streams Service.

### Changed
- `AWS.DynamoDB` module has updated documentation.

## [v0.0.2] - 2015-07-09
### Added
- `AWS.CodeCommit` module for CodeCommit Service.
- `AWS.CodePipeline` module for CodePipeline Service.
- `AWS.CognitoIdentity` module for Cognito Service.
- `AWS.DirectoryService` module for Directory Service.
- `AWS.Route53Domains` module for Route53 Domains Service.
- `AWS.Workspaces` module for Workspaces Service.

### Changed
- `AWS.CodeDeploy` module has new functionality for managing on premises
  instances.
- `AWS.Config` module has updated documentation.
- `AWS.DynamoDB` module has updated documentation.
- `AWS.ECS` module has updated documentation and new support for the
  `UpdateContainerAgent` action.
- `AWS.Kinesis` module has updated documentation.
- `AWS.KMS` module has updated documentation and new support for the
  `UpdateAlias` action.
- `AWS.Logs` module has updated documentation and new functionality for
  managing log events and subscription filters.
- `AWS.OpsWorks` module has updated documentation and new support for the
  `DescribeAgentVersions` and `GrantAccess` actions.
- `AWS.SSM` module has updated documentation.
- `AWS.StorageGateway` module has updated documentation and new support for
  the `ListVolumeInitiators` action.

## [v0.0.1](https://github.com/jkakar/aws-elixir/tree/v0.0.1) - 2015-05-29
### Added
- `AWS.CloudHSM` module for CloudHSM Service.
- `AWS.CloudTrail` module for CloudTrail Service.
- `AWS.CodeDeploy` module for CodeDeploy Service.
- `AWS.Config` module for Config Service.
- `AWS.DataPipeline` module for DataPipeline Service.
- `AWS.DirectConnect` module for DirectConnect Service.
- `AWS.DynamoDB` module for DynamoDB Service.
- `AWS.ECS` module for EC2 Container Service.
- `AWS.EMR` module for Elastic MapReduce Service.
- `AWS.KMS` module for Key Management Service.
- `AWS.Kinesis` module for Kinesis Service.
- `AWS.Logs` module for CloudWatch Logs Service.
- `AWS.OpsWorks` module for OpsWorks Service.
- `AWS.SSM` module for Simple Systems Management Service.
- `AWS.SWF` module for Simple Workflow Service.
- `AWS.StorageGateway` module for Storage Gateway Service
- `AWS.Support` module for Support Service.

[unreleased]: https://github.com/jkakar/aws-elixir/compare/v0.0.6...HEAD
[v0.0.6]: https://github.com/jkakar/aws-elixir/compare/v0.0.5...v0.0.6
[v0.0.5]: https://github.com/jkakar/aws-elixir/compare/v0.0.4...v0.0.5
[v0.0.4]: https://github.com/jkakar/aws-elixir/compare/v0.0.3...v0.0.4
[v0.0.3]: https://github.com/jkakar/aws-elixir/compare/v0.0.2...v0.0.3
[v0.0.2]: https://github.com/jkakar/aws-elixir/compare/v0.0.1...v0.0.2
