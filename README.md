# Cloud Factory Provisioning
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/grendel-consulting/cloud-factory-provisioning/badge)](https://scorecard.dev/viewer/?uri=github.com/grendel-consulting/cloud-factory-provisioning)


Co-ordination and extensibility whilst vending using with the Account Factory for Terraform (AFT) framework. Further customisation, beyond that provided by the vending process, through an AWS Step Function State Machine, which enables control flow and integration with AWS and third-party services.

## Usage

### State Machine

Define your own state machine, which will receive a [JSON payload](https://github.com/aws-ia/terraform-aws-control_tower_account_factory/tree/main/sources/aft-customizations-repos/aft-account-provisioning-customizations#example-payload) containing the account request information and state of the AWS Account being created.

## Deployment

Deployment occurs on merge to main, triggering an AWS CodePipeline in the factory management OU; it is not speculatively planned through GitHub Actions as the buildspec hydrates the providers and backends through the Jinga templates.

## Further Reading

See: [AFT Account Provisioning Customizations](https://github.com/aws-ia/terraform-aws-control_tower_account_factory/tree/main/sources/aft-customizations-repos/aft-account-provisioning-customizations)
