# coglinc github settings

This repository defines basic, shareable settings for repositories owned by this organization.


## Usage

Files defined in [.github](.github/) (excluding [settings.yml](.github/settings.yml)) contain configurations that can be
extended by other repositories in this organization. For more details, see [probot-config/recipes](https://github.com/probot/probot-config#recipes). 


## Contributing

### Testing locally

:warning: This requires [act](https://github.com/nektos/act)

- To simulate a push event that does not modify the `.github/organization/members.yml` file:

  `act -e .act/push-no-members-file-modifications.json -s ORG_MEMBERSHIP_MANAGEMENT_TOKEN=[personal access token]`
  
- To simulate a push event that modifies the `.github/organization/members.yml` file:

  :white_check_mark: The action will still use your local file
  
  `act -e .act/push-members-file-modifications.json -s ORG_MEMBERSHIP_MANAGEMENT_TOKEN=[personal access token]`

### Validation

To validate settings, simply run `npm run lint`.

### Github workflows

To validate Github workflows before pushing a PR, simply run `npm run lint:workflows`.
