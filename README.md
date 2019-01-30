# JFrog GoCenter
![JFrog GoCenter Logo](./resources/logo.png)


If you are reading this, then hopefully you have an interest in immutable re-usable Go modules, so welcome to JFrog GoCenter.  If
you haven't already, you can check out the actual web page at [gocenter.io](https://gocenter.io), but you may as
well stick around and read this page first.

## The documentation on what is GoCenter, how GoCenter works, how to set up your tools to work with GoCenter and the Fequently Asked Questions (and answers!) can be found in [the Wiki of the project](https://github.com/jfrog/gocenter/wiki).

## Troubleshooting

### I pointed `GOPROXY` to GoCenter (https://gocenter.io), but now my build is failing.

The Go client fails if at least one dependency can’t be found at `GOPROXY`. We recommend using `goc` instead of `go` to build your projects with GoCenter. For example: `goc build`. This is more fully explained in the [Using goc wiki page](https://github.com/jfrog/gocenter/wiki/Using-goc).

### I’m running into “checksum mismatch” errors in my build while resolving from GoCenter.

This issue can be easily fixed by removing the corresponding entry in your `go.sum` file that is causing the error or removing your `go.sum` file completely, then rerunning your build again to regenerate the checksums correctly. A detailed explanation including why this error occurs is provided in the [FAQ wiki page](https://github.com/jfrog/gocenter/wiki/Frequently-Asked-Questions).

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
* For issues relating to `goc` client, please file a GitHub issue on the [goc GitHub repository](https://github.com/jfrog/goc)
* If you have found a security vulnerability in any part of GoCenter or its infrastructure, please e-mail security@jfrog.com

## Contributing to GoCenter

Please check our [Contributing Guide](https://github.com/jfrog/gocenter/blob/master/CONTRIBUTING.md).

## Legal & Other Links
* The [Terms of Service](https://gocenter.jfrog.com/terms) for JFrog GoCenter
* The JFrog GoCenter [Privacy Policy](https://gocenter.jfrog.com/privacypolicy)
