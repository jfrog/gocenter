# JFrog GoCenter
![JFrog GoCenter Logo](https://raw.githubusercontent.com/jfrog/gocenter/master/resources/logo.png)

# Attention: Deprecation notice for Bintray, GoCenter, and ChartCenter. [Learn More](#)

If you are reading this, then hopefully you have an interest in immutable re-usable Go modules, so welcome to JFrog GoCenter.  If
you haven't already, you can check out the actual web page at [gocenter.io](https://gocenter.io), but you may as
well stick around and read this page first.

## The documentation on what is GoCenter, how GoCenter works, how to set up your tools to work with GoCenter and the Frequently Asked Questions (and answers!) can be found in [the Wiki of the project](https://github.com/jfrog/gocenter/wiki).

## Troubleshooting

### I’m running into “checksum mismatch” errors in my build while resolving from GoCenter.

Be very careful with checksum mismatches. Except of one case, detailed in our [FAQ wiki page](https://github.com/jfrog/gocenter/wiki/Frequently-Asked-Questions), it usually means you have downloaded a damaged dependency module.

## Release Notes

GoCenter is constantly improving your experience with Go Modules based on community feedback. We make lots of small improvements regularly and keep a running list of major ones in our releases.md file. Stay up to date with us by checking out our latest: [Release Notes](https://github.com/jfrog/gocenter/blob/master/releases.md).

## Contact us

* Twitter: ping us `@jfrog`.
* Slack: find us in `#gocenter` channel in the [Gopher Slack](https://invite.slack.golangbridge.org/).
* Email: shoot us an email to `gocenter@jfrog.com`

### Reporting Technical Issues with GoCenter

* Please open an issue on this repository for any issues you experience while using our service, or any improvements you wish to discuss.
  * When opening an issue, please make clear if it is a bug/problem you are experiencing or a request for a new feature or improvement
  * If you are submitting a bug report, please provide detailed steps to reproduce your issue.  This should include the name of the module and the version that you were searching for/trying to add/trying to consume if relevant.
  * To open an issue click 'Issues' above and please review the list of open issues.
    * If your issue already exists, please select that issue and add any additional information that might help us resolve it, or click the reactions button and thumbs up (+1) if you want to indicate you are also experiencing this issue, but have no new information to add.
    * If your issue/improvement is not on the list, please click the 'New Issue' button and provide details
* If your issue is not appropriate for a public discussion, please contact us via e-mail at gocenter@jfrog.com.
* If you have issues integrating Artifactory with JFrog GoCenter, and you have support, please file a support ticket.
* For issues relating to the JFrog CLI, please file a GitHub issue on the [jfrog-cli-go GitHub repository](https://github.com/jfrog/jfrog-cli-go)
* If you have found a security vulnerability in any part of GoCenter or its infrastructure, please e-mail security@jfrog.com

## Contributing to GoCenter

Please check our [Contributing Guide](https://github.com/jfrog/gocenter/blob/master/CONTRIBUTING.md).

## Legal & Other Links
* The [Terms of Service](https://gocenter.jfrog.com/terms) for JFrog GoCenter
* The JFrog GoCenter [Privacy Policy](https://gocenter.jfrog.com/privacypolicy)
