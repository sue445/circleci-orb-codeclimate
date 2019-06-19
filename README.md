# circleci-orb-codeclimate
CircleCI orb for [Code Climate](https://codeclimate.com/)

https://circleci.com/orbs/registry/orb/sue445/codeclimate

[![CircleCI](https://circleci.com/gh/sue445/circleci-orb-codeclimate/tree/master.svg?style=svg)](https://circleci.com/gh/sue445/circleci-orb-codeclimate/tree/master)

## Example
```yml
version: 2.1

orbs:
  codeclimate: sue445/codeclimate@x.y.z

jobs:
  test:
  environment:
    CC_TEST_REPORTER_ID: YOUR_CODE_CLIMATE_REPORTER_ID
  
    steps:
      - checkout
  
      - with-cc-test-reporter:
          after_build_args: "--coverage-input-type simplecov"
  
          steps:
            - run: bundle exec rspec
```

## Details
https://docs.codeclimate.com/docs/configuring-test-coverage
