# Release Notes

<!-- MarkdownTOC autolink="true" bracket="round" -->

- [2019 October 25: Better discoverability](#2019-october-25-better-discoverability)
- [2019 October 7: New metrics panel and new Go Center look](#2019-october-7-new-metrics-panel-and-new-Go-Center-look)
- [2019 September 10: Checksum database support in GoCenter](#2019-september-10-checksum-database-support-in-gocenter)
- [2019 July 23: Released GoCenter module page](#2019-july-23-released-gocenter-module-page)
- [2019 June 12: Display module information in search results](#2019-june-12-module-information-in-search-results)
- [2019 June 6: Improved search functionality](#2019-june-6-improved-search-functionality)
- [2019 March 27: Enhanced automatic inclusion of Go modules](#2019-march-27-enhanced-automatic-inclusion-of-go-modules)
- [2019 March 14: Updated logic for generating mod files](#2019-march-14-updated-logic-for-generating-mod-files)
- [2019 January 28: GA](#2019-January-28-ga)

<!-- /MarkdownTOC -->

## 2019 October 25: Better discoverability
On this release, we added full-text search capabilities so that users can search for modules based on their descriptions in the main search bar. A few other updates include:

* We enhanced the way we detect licenses - now we will list more than one license if available for modules
* Update: If a request is made to fetch a forked module for which the go.mod file refers to parent module, GoCenter should return 404 for the bad module but still send a request to processor for the go.mod file
* Bug fix: Scoring check condition - modules taken down due to http 451 errors should be reflected in the condition to detect during score computation

## 2019 October 7: New metrics panel and new Go Center look
A new version of GoCenter was released today. Apart from the look and feel changes, there is a new metrics panel that will  help module authors and users access additional metadata to make better decisions around which modules to use. Check it out - https://search.gocenter.io/stats

Other updates included a new improved homepage image and:
* Top bar has been changed from green to black to match the new unified experience look and feel 
* The navigation menu has been expanded to include versions and metrics visible in the UI from the start
* White information bar includes new metrics data including license information
* A blog link has been added to the top bar.

## 2019 September 10: Checksum database support in GoCenter
In this release, we started supporting the checksum database by proxying sum.golang.org. So if you upgraded Go to 1.13 and have the proxy already set to https://gocenter.io, then the sumdb requests from the Go client will also be served by gocenter.io. As part of this release, we also:
 *	modified package.json
 *	Metrics tab update
 *	Added get module names API

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


## 2019 June 12: Module information in search results
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

## 2019 March 27: Enhanced automatic inclusion of Go modules 
In this release, GoCenter has enhanced the automatic inclusion of Go modules
* GoCenter will now automatically attempt to include missing Go modules that were requested at least once
* This means that if a user tries to retrieve a dependency from GoCenter, but receives a 404 error (“Not Found”) because the module does not yet exist in GoCenter, a background process in GoCenter will eventually try to include that module through the [Inclusion Request process](https://github.com/jfrog/gocenter/wiki/How-GoCenter-Works#inclusion-process). 
* This feature will enhance the user experience of GoCenter as a Go proxy by reducing the occurrence of 404 errors in your builds.

## 2019 March 14: Updated logic for generating mod files 
In this release, GoCenter has changed the logic of mod files generation. 
* GoCenter will no longer generate a populated go.mod file for Go projects that haven’t yet opted into modules and do not yet contain a go.mod file. Prior to this release, GoCenter was using a different approach to produce missing go.mod files, to achieve optimal reproducibility. However, after further discussion with the Go community, and considering that the initial approach may cause the go.mod file’s checksum to be different from what may have been recorded in a project’s go.sum before using GoCenter, GoCenter will now generate empty go.mod files for Go projects that haven’t yet opted into modules.
* As part of this release, go.mod files that were previously generated by GoCenter will be converted to be consistent with this new behavior.
* For Go projects that already have go.mod files, GoCenter will continue to keep these .mod files unchanged when processing them to be included in GoCenter.

## 2019 January 28: GA
* GoCenter.io goes live!
* Basic ability to search for modules
* Basic ability to request new modules be added to GoCenter
* Basic ability to determine the status of a module/version
*	New CLI version
*	Updated the UI
*	Created helper to fix Artifactory mod files
*	Updated main view mobile layout
