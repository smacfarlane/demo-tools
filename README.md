# Assumptions

* Scripts are executed from a Windows workstation in a BJC demo environment
* Demo environment is in us-west-2

# Usage

Clone this repository.

Run `./bootstrap.ps1 PASSWORD` to create a windows instance that is vulnerable to wannacry.
Validate in the Automate Compliance tab when bootstrapping is finished. 

## Remediation
Edit `roles/teardrop.json` and add `tissues` to the `run_list`
Upload the role with `knife role from file roles/teardrop.json`
Execute the remediation script with the same password used for bootstrapping. `./remediate.ps1 PASSWORD`

