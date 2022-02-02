# Black Duck CoPilot Packrat/Travis CI Example
Example project for setting up CoPilot with a Packrat (R) Project Built using Travis CI

[![Build Status](https://travis-ci.org/BlackDuckCoPilot/example-packrat-travis.svg?branch=master)](https://travis-ci.org/BlackDuckCoPilot/example-packrat-travis) [![Black Duck Security Risk](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-packrat-travis/branches/master/badge-risk.svg)](https://copilot.blackducksoftware.com/github/repos/BlackDuckCoPilot/example-packrat-travis/branches/master)

Shows a working setup for using Synopsys CoPilot to analyze the risk of project dependencies

## Travis CI Setup
The `.travis.yml` file has been modified to upload generated dependency data to CoPilot:
```yaml
after_success:
  - bash <(curl -s https://copilot.blackducksoftware.com/ci/travis/scripts/upload)
```
