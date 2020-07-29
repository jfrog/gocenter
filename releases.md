# Release Notes

<!-- MarkdownTOC autolink="true" bracket="round" -->
## 2020 July 27: Top Modules API and GoDocs breadcrumbs
- [2020 July 27: Top Modules API and GoDocs breadcrumbs](#2020-july-27-top-modules-api-and-godocs-breadcrumbs)
- [2020 July 21: GoDocs added and increased support](#2020-july-21-godocs-added-and-increased-support)
- [2020 June 19: Helm 3 compliance](#2020-june-19-helm-3-compliance)
- [2020 June 3: Minor changes](#2020-june-3-minor-changes)
- [2020 May 30: Sitemap and IDE updates](#2020-may-30-sitemap-and-ide-updates)
- [2020 May 19: GoCenter updates](#2020-may-19-gocenter-updates)
- [2020 May 1: GoCenter security in VSCode extension](#2020-may-1-gocenter-security-in-vscode-extension)
- [2020 April 3: API provisioning and bug fixes](#2020-april-3-api-provisioning-and-bug-fixes)
- [2020 March 13: UI performance](#2020-march-13-ui-performance)
- [2020 February 14: Minor fixes](#2020-february-14-minor-fixes)
- [2020 January 16: Pseudo-versions fix](#2020-january-16-pseudo-versions-fix)
- [2020 January 7: Xray scans gocenter](#2020-january-7-xray-scans-gocenter)
- [2019 December 18: Improved handling](#2019-december-18-improved-handling)
- [2019 December 17: User interface improvements](#2019-december-17-user-interface-improvements)
- [2019 October 25: Better discoverability](#2019-october-25-better-discoverability)
- [2019 October 17: Bug fixes and regular maintenance for Go](#2019-october-17-bug-fixes-and-regular-maintenance-for-go)
- [2019 October 9: More UI improvements](#2019-october-9-more-ui-improvements)
- [2019 October 7: New Metrics Panel and New Go Center Look](#2019-october-7-new-metrics-panel-and-new-GoCenter-look)
- [2019 September 19: SEO improvements](#2019-september-19-seo-improvements)
- [2019 September 10: Checksum database support in GoCenter](#2019-september-10-checksum-database-support-in-gocenter)
- [2019 September 3: Beginning to build a Go Modules Score](#2019-september-3-beginning-to-build-a-go-modules-score)
- [2019 August 27: Discovery process updates](#2019-august-27-discovery-process-updates)
- [2019 July 23: Released GoCenter module page](#2019-july-23-released-gocenter-module-page)
- [2019 June 12: Display module information in search results](#2019-june-12-display-module-information-in-search-results)
- [2019 June 6: Improved search functionality](#2019-june-6-improved-search-functionality)
- [2019 May 24: Go version updates](#2019-may-24-go-version-updates)
- [2019 April 26: Improve Go Module metadata and search](#2019-april-26-improve-go-module-metadata-and-search)
- [2019 March 27: Enhanced automatic inclusion of Go modules](#2019-march-27-enhanced-automatic-inclusion-of-go-modules)
- [2019 March 20: Inclusion, discovery, validation](#2019-march-20-inclusion-discovery-validation)
- [2019 March 14: Updated logic for generating mod files](#2019-march-14-updated-logic-for-generating-mod-files)
- [2019 March 9: Fixed incompatibility](#2019-march-9-fixed-incompatibility)
- [2019 February 7: Optimized discovery and support for Jenkins](#2019-february-7-optimized-discovery-and-support-for-jenkins)
- [2019 January 28: GA](#2019-January-28-GA)

<!-- /MarkdownTOC -->

## 2020 July 27: Top Modules API and GoDocs breadcrumbs
Some minor work was done to fix breadcrumbs as well as the API that shows the upcoming top modules. Summary:

* Top Modules API was updated to reflect the new scope of look and feel changes
* Under certain conditions, metadata service was not handling shutdowns well. This issue has been addressed.
* GoDocs breadcrumb fixed
* Dependency tab was not updated if a different version was selected. Only the counts were being updated. This issue has been fixed.

## 2020 July 21: GoDocs Added and Increased Support
We've just added a GoDocs tab to all the module pages! We've also added updates for Go 1.14 : 

* Supporting Go 1.14 while handling advance 404 requests for transitive dependencies.
* Supporting force capability if GoDocs needs to be regenerated due to bugs in GoDoc tool.

## 2020 June 19: Helm 3 compliance
GoCenter is now compliant with Helm 3. These updates encompass:

* Backend changes neeed for the new landing page have been completed. Look out for this on the UI soon!
* More sitemap.xml changes. It was a great learning experience and will help us improve how SEO works on the site.
* GoCenter is now only using Helm 3 - bye bye tiller! We're fully helm v3 compliant.

## 2020 June 3: Minor changes

* We're now filtering out v0.0.0 module processing requests from the IDE
* Remove time from sitemap.xml
* Xray URL changes

## 2020 May 30: Sitemap and IDE updates
GoCenter and the IDE were upgraded with a few changes. What was rolled out:

* sitemap auto-generation. Newly added modules will be automatically included to the sitemap (sitemap-modules.xml) 
* new announcement added to the landing page
* IDE bug and enhancement. We realized we can enhance the inclusion mechanism to address 404s when a module is requested in the IDE, but not availabe in GoCenter. This way additional metadata will be available to developers who are using the IDE plugin but didn't set GOPROXY to gocenter before rebuilding their cache.

## 2020 May 19: GoCenter updates
GoCenter just added an announcements area to the UI, is on its way to adding GoDocs, and made a few other minor UI updates and finished up a few other back-end upgrades. Overall updates include:

* Pseudo-version Github fix
* GoDocs back-end completed
* Remove relative links in docs
* Kubernetes and infrastructure upgrades
* Added an announcements area

## 2020 May 1: GoCenter security in VSCode extension
We're really excited to be able to provide a new free security feature from GoCenter now in the JFrog Extension for VSCode. With vulnerability scanning becoming a prominent part of GoCenter's UI in early 2020, we're now bringing parts of this experience to Visual Studio Code so developers can keep their Go Modules secure right when they're coding. Here is what you can now see for free right in the IDE: 

* Total number of issues for each Go Module and version
* Severity level with color-coded dots showing high, medium, and low issues
* Stars, license information, latest version, and a snippet from the module's readme
* Ability to see vulnerability alerts for module dependencies
* Direct links to GoCenter tabs for more details including CVE and issue description

You can find this extension in the VSCode marketplace under "JFrog" or [download it here](https://marketplace.visualstudio.com/items?itemName=JFrog.jfrog-vscode-extension). Need more information? Read the [launch blog to learn even more!](https://jfrog.com/blog/free-go-module-vulnerability-scanning-in-visual-studio-code/)

## 2020 April 3: API provisioning and bug fixes
Over the last two weeks, we've been provisioning an API to be used in an upcoming IDE release for GoCenter as well as making minor updates to the UI and social + bug fixes.

* IDE UI API versioning
* Added error string to API struct
* Autofocus active tab fix
* Updated Twitter handle: @gocenterio

## 2020 March 13: UI performance
We've updated a few of the front-end and back-end elements of the UI.

* Performance improvements include deep-linking into individual tabs such as security and metrics
* URL restructuring
* Metadata updates

## 2020 February 14: Minor fixes
The team noticed few minor issues with name changes in GitHub. We've updated our logic. 

* Projects can be renamed on GitHub, and GoCenter should be able to detect these changes to provide the right information. We created logic to detect source location name changes.
* For a few rare scenarios, GoCenter was showing errors from the wrong modules. Now fixed.
* GoCenter was not able to process the go-get meta tag for multi modules repos like cloud.google.com/go. We’ve fixed this.

## 2020 January 16: Pseudo-versions fix
GoCenter supports multiple module versions from 1.13 to all prior versions such as 1.12. Starting from Go 1.13, the Go client verifies the pseudo-version components against the version control metadata.

Go versions before 1.13 do not enforce these rules about pseudo-version components. This means that, even though users were not supposed to generate pseudo-versions manually, they could have the same commit hash being used in multiple pseudo-versions without any issues. 

* We have just addressed and fixed this in GoCenter!

Read More: https://dev.to/elioengcomp_41/gocenter-1-12-and-1-13-incorrect-pseudo-versions-fix-o4g

## 2020 January 7: Xray scans GoCenter
GoCenter now includes vulnerability scanning in the UI!

Now, every module and version in GoCenter is automatically scanned for known vulnerabilities recognized in public vulnerability databases such as NVD. Those results are stored in GoCenter and exposed on the Security page of the UI, which will list all vulnerabilities that exist in the module version.

Learn more: https://jfrog.com/blog/gocenter-reveals-go-module-vulnerabilities-with-xray/

## 2019 December 18: Improved handling
Go Center:
* Improved how it handles cases for module versions that are +incompatible, but are still in v1 or v0.

## 2019 December 17: User interface improvements
We fixed a few minor issues in the UI and added an exciting new feature to highlight great modules:
* Improved error-handling transparency on versions page that allows users to download full txt log when version uploads error
* Keep an eye out for Go Badges! A new feature that will begin highlighting module authors that are creating great projects!
* Gosumdb entries for modules with uppercase values were not being cached. This has been fixed.

## 2019 October 25: Better discoverability
On this release, we added full-text search capabilities so that users can search for modules based on their descriptions in the main search bar. A few other updates include:

* We enhanced the way we detect licenses - now we will list more than one license if available for modules
* Update: If a request is made to fetch a forked module for which the go.mod file refers to parent module, GoCenter should return 404 for the bad module but still send a request to processor for the go.mod file
* Bug fix: scoring check condition - modules taken down due to http 451 errors should be reflected in the condition to detect during score computation

## 2019 October 17: Bug fixes and regular maintenance for Go
This week we made some improvements to SEO and fixed a few other items:
* We adjust the weights for criteria for Go Module scoring
* Upgraded Kubernetes to patch security issue
* Metadata service to trigger lookup calls for new module versions against gosumdb.
* Updated Go version to patch security issue

## 2019 October 9: More UI improvements
On this release, we made lots of small changes to the Go Center UI. We've added minor improvements to all the content that we released earlier this month including a few elements of how the home page looks. Other improvements include:
* Fixed source location discovery and added API to fix data
* Updated Go version
* Added SEO keywords to header
* Stats calculated text alignment
* Updated autosuggest styles
* Updated homepage image from microscope to frog and gopher
* Discovery ignoring tags with + suffix

## 2019 October 7: New metrics panel and new GoCenter look
A new version of GoCenter was released today. Apart from the look and feel changes, there is a new metrics panel that will  help module authors and users access additional metadata to make better decisions around which modules to use. Check it out - https://search.gocenter.io/stats

Other updates included a new improved homepage image and:
* Top bar has been changed from green to black to match the new unified experience look and feel 
* The navigation menu has been expanded to include versions and metrics visible in the UI from the start
* White information bar includes new metrics data including license information
* A blog link has been added to the top bar.

## 2019 September 19: SEO improvements
We've been improving the SEO experience with changes to the content and UI
 *	Added a new CLI version
 *	GoCenter search description update for SEO
 *	Scoring tab updates

## 2019 September 10: Checksum database support in GoCenter
In this release, we started supporting the checksum database by proxying sum.golang.org. So if you upgraded Go to 1.13 and have the proxy already set to https://gocenter.io, then the sumdb requests from the Go client will also be served by gocenter.io. As part of this release, we also:
 *	modified package.json
 *	Metrics tab update
 *	Added get module names API
 
## 2019 September 3: Beginning to build a Go Modules Score
Today we released our first version of the GoScore which helps provides us data to measure the quality and quantity of Go modules. Learn more here: https://github.com/jfrog/gocenter/wiki/Module-Scoring

## 2019 August 27: Discovery process updates
In this release, we fixed a few issues regarding the discovery request process. Both discovery and getModules API will validate if module name is declared in the go.mod file of a tag – if it is compatible with the project being checked. If they are not compatible, the tag will be ignored. Other improvements on this release include:
 *	do a lookup on Artifactory sumdb virtual repo during metadata update.
 *	Check git url before trying to fetch tags
 *	Fix github link for pseudo versions

## 2019 July 23: Released GoCenter module page
In this release, GoCenter has:
* Introduced a module page. As a one-stop central Go modules repository, GoCenter now provides more module information to developers to decide whether to use this module as a dependency in a project. Each module in GoCenter now has five tabs to show information:
  * README: Developers care about documentation, so the first page you land on is the README documenting the module
  * Mod file: This tab shows the contents of the `go.mod` file or, if the module has not adopted Go modules yet, GoCenter will  recommend a mod file based on `go mod tidy` for the latest version of the module available in GoCenter.
  * Dependencies: This tab shows all of the module’s dependencies in a dependency tree format.
  * Used by: This tab shows which other projects use the selected module
  * Versions: This tab shows all the versions that GoCenter knows about, and has a copy of, ready to serve to developers.
* Changed the way Go modules are resolved. If the module isn’t in GoCenter, it will get the module from the source for you. This feature limits the number of HTTP/404 responses and means developers no longer need any additional tools to get all their public modules from GoCenter.
* Updated the `Set Me Up` page to include instructions for Windows PowerShell and the traditional Windows terminal.

## 2019 June 12: Display module information in search results
In this release, module metadata will be displayed as part of search results. Other fixes that came out today include:
*	Deep processing when shallow processing times out.	
*	Added module update retries		
*	Log expired locks		
*	Fixed virtual repo composition

## 2019 June 6: Improved search functionality
In this release, GoCenter has enriched the search functionality which includes most relevant Go modules in search results. Other updates include:
*	Ignore build constraint validation failure
*	Fixed elastic json escape bug
*	Added support to Artifactory 6.10.x
*	Added support to modules with .go in their names
 
## 2019 May 24: Go version updates
This month we’re continuing to make updates to Go Center that incorporate changes from Go 1.12. Some issues addressed in this release include:
*	Optimize searches for scalability (such as using Elasticdb)
*	Fixed module indexing issues		
* tidying up how we show go.mod file information on the UI
*	Init cache provider for metadata service
*	module metrics in module status

## 2019 April 26: Improve Go Module metadata and search
The focus here was on adding module metadata services and improving the search experience. Updates include:
*	Initial version source location metadata job			
*	Changed elastic client and added new source location metadata		
*	Added metrics daos				
*	Created metadata microservice		
*	Elastic added to devenv		
*	Removed plus suffixed tags from missing		
*	Changed elastic client and added new source location metadata

## 2019 March 27: Enhanced automatic inclusion of Go modules 
In this release, GoCenter has enhanced the automatic inclusion of Go modules
* GoCenter will now automatically attempt to include missing Go modules that were requested at least once
* This means that if a user tries to retrieve a dependency from GoCenter, but receives a 404 error (“Not Found”) because the module does not yet exist in GoCenter, a background process in GoCenter will eventually try to include that module through the [Inclusion Request process](https://github.com/jfrog/gocenter/wiki/How-GoCenter-Works#inclusion-process). 
* This feature will enhance the user experience of GoCenter as a Go proxy by reducing the occurrence of 404 errors in your builds.

## 2019 March 20: Inclusion, discovery, validation
Lots of Bug fixes. Inclusion, discovery, validation. A few other updates over the last two weeks include:
* Init shared cache provider for discovery microservice
* Fixed missing dependency injection
* Added version existence check, module name and version decoding Added inclusion request rules caching and github quota check * Initial inclusion request refactoring 
* Event validation rules 
* Create job structure initial version
* Added version existence check, module name and version decoding
* Fixed go.sum file

## 2019 March 14: Updated logic for generating mod files 
In this release, GoCenter has changed the logic of mod files generation. 
* GoCenter will no longer generate a populated go.mod file for Go projects that haven’t yet opted into modules and do not yet contain a go.mod file. Prior to this release, GoCenter was using a different approach to produce missing go.mod files, to achieve optimal reproducibility. However, after further discussion with the Go community, and considering that the initial approach may cause the go.mod file’s checksum to be different from what may have been recorded in a project’s go.sum before using GoCenter, GoCenter will now generate empty go.mod files for Go projects that haven’t yet opted into modules.
* As part of this release, go.mod files that were previously generated by GoCenter will be converted to be consistent with this new behavior.
* For Go projects that already have go.mod files, GoCenter will continue to keep these .mod files unchanged when processing them to be included in GoCenter.

## 2019 March 9: Fixed incompatibility
This release focused on bug fixes and included fixing scenario incompatibility issues. Updates:
* Fix double +incompatible versions creation
* Initial inclusion request refactoring		
* Event validation rules		
* Added module list query

## 2019 February 7: Optimized discovery and support for Jenkins
We updated and fixed some core features. We focused on optimized discovery. More Updates include:
* Converted production cluster from zonal to regional
* Added retry mechanisms during processing
* Check for max number of tags before getting another page of tags
* Add regional stage and prod clusters support for Jenkins deploy		
* Fixed feature pipeline 
* Introduced retries and checks for CLI timeouts
* Updated caddy_helm_pkg_feat.sh and add debug for other Jenkins files
* Sdd regional stage and prod clusters support for Jenkins deploy		
* Trigger CI pipeline

## 2019 January 28: GA
GoCenter.io goes live!
* Basic ability to search for modules
* Basic ability to request new modules be added to GoCenter
* Basic ability to determine the status of a module/version
*	New CLI version
*	Updated the UI
*	Created helper to fix Artifactory mod files
*	Updated main view mobile layout
