<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [oomph-catalogue
](#oomph-catalogue)
  - [Setup](#setup)
  - [Example walkthrough](#example-walkthrough)
  - [Example status](#example-status)
    - [C:\Users\Reichert\.p2](#c\users\reichert\p2)
      - [pools.info](#poolsinfo)
      - [profiles.info](#profilesinfo)
    - [C:\_oomph_agent](#c\_oomph_agent)
      - [pools.info](#poolsinfo-1)
      - [profiles.info](#profilesinfo-1)
    - [C:\Users\Reichert\.eclipse\org.eclipse.oomph.p2](#c\users\reichert\eclipse\orgeclipseoomphp2)
      - [agents.info](#agentsinfo)
      - [defaults.info](#defaultsinfo)
    - [C:\Users\Reichert\.eclipse\org.eclipse.oomph.p2\setups](#c\users\reichert\eclipse\orgeclipseoomphp2\setups)
      - [catalogs.setup](#catalogssetup)
      - [locations.setup](#locationssetup)
      - [user.setup](#usersetup)
  - [Example for creating a new Oomph setup](#example-for-creating-a-new-oomph-setup)
    - [Initial steps](#initial-steps)
    - [General hints](#general-hints)
    - [Start configuration](#start-configuration)
    - [Compile configuration](#compile-configuration)
    - [IDE features and plug-ins selection](#ide-features-and-plug-ins-selection)
    - [IDE preferences](#ide-preferences)
    - [Git clone](#git-clone)
    - [Projects Import](#projects-import)
    - [Launcher](#launcher)
    - [Targlets / Target platform](#targlets--target-platform)
    - [Working sets](#working-sets)
    - [Mylyn](#mylyn)
    - [Streams](#streams)
    - [Tasks not used yet in this example](#tasks-not-used-yet-in-this-example)
  - [Example for executing Oomph setup](#example-for-executing-oomph-setup)
    - [Product](#product)
    - [Projects](#projects)
    - [Variables](#variables)
    - [Confirmation](#confirmation)
    - [In installed IDE](#in-installed-ide)
  - [Resources](#resources)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

oomph-catalogue
===============

Custom product and project catalogue for my GitHub projects, inspired by [Alex' oomph setups](https://github.com/nittka/oomph-playground).

## Setup

 * download the [Oomph installer](http://wiki.eclipse.org/Eclipse_Oomph_Installer) 
 * add the following line to the installer's oomph.ini

`-Doomph.redirection.setups=http://git.eclipse.org/c/oomph/org.eclipse.oomph.git/plain/setups/->https://raw.githubusercontent.com/joergreichert/oomph-catalogue/master/setups/`

 * start the Oomph installer
 
## Example walkthrough
 * 1.0.0 Build 718
 * page 1
   * Switch to advanced mode by clicking on the tools icon (first icon in the upper right corner) (this will close the current window an open a new window; you can always return to simple mode by clicking on the 4th icon in lower left corner) (if you don't see a tools icon in upper right corner, you are already in advanced mode)
   * Click on the 5th icon in lower left corner to update the current Oomph installation (if the icon shows an hourclass in the upper right corner, wait, as Oomph is still checking if there are new updates available - if there are updates the icon will be coloured and animated, if there are no updates available the icon will be gray) 
   * Eclipse.org
     * Eclipse Standard/SDK
   * Product version: Latest Release (Luna)
   * Bundle Pool (Check): C:\_oomph_bundle_pool
     * Manage Bundle Pools...
	   * Setup
         * New Agent: C:\_oomph_agent
	     * New Bundle Pool: C:\_oomph_bundle_pool
	   * Config	 
	     * C:\_oomph_agent
	       * C:\_oomph_bundle_pool
	     * C:\Users\.p2
		   * pool
 * page 2
   * Press refresh button in the upper right corner
   * Joerg-Projects
     * Joerg's Github projects
           * [ActiveAnnotationsExamples](https://github.com/joergreichert/ActiveAnnotationsExamples) [oomph.setup](https://raw.githubusercontent.com/joergreichert/ActiveAnnotationsExamples/master/_common/de.abg.jreichert.activeanno.parent/oomph.setup)   
           * [RepositoryTargetGenerator](https://github.com/joergreichert/RepositoryTargetGenerator) [oomph.setup](https://raw.githubusercontent.com/joergreichert/RepositoryTargetGenerator/master/releng/de.abg.jreichert.repositorytarget.config.parent/oomph.setup)   
           * [mobilecloud-14-xtend](https://github.com/joergreichert/mobile-14-xtend) [oomph.setup](https://raw.githubusercontent.com/joergreichert/mobilecloud-14-xtend/master/oomph.setup)   
           * [OperaMisterWongBookmarks](https://github.com/joergreichert/OperaMisterWongBookmarks) [oomph.setup](https://raw.githubusercontent.com/joergreichert/OperaMisterWongBookmarks/master/de.abg.jreichert.bookmarks.config.parent/oomph.setup)   
           * [OperationsResearch](https://github.com/joergreichert/OperationsResearch) [oomph.setup](https://raw.githubusercontent.com/joergreichert/OperationsResearch/master/releng/org.eclipse.xtext.example.knapsack.config.parent/oomph.setup)   
           * [XtextPlayground](https://github.com/joergreichert/XtextPlayground) [oomph.setup](https://raw.githubusercontent.com/joergreichert/XtextPlayground/master/TODO_Example_Xtext2/releng/org.eclipse.xtext.todo.config.parent/oomph.setup)   
           * [Permet](https://github.com/joergreichert/Permet) [oomph.setup](https://raw.githubusercontent.com/joergreichert/Permet/master/releng/org.eclipse.xtext.example.fowlerdsl.config.parent/oomph.setup)   
           * [Cool](https://github.com/joergreichert/Cool) [oomph.setup](https://raw.githubusercontent.com/joergreichert/Cool/master/oomph.setup)   
           * [Spray](https://code.google.com/p/spray/) [oomph.setup](http://spray.eclipselabs.org.codespot.com/git-history/luna/devtools/org.eclipselabs.spray.releng.tools/Spray.setup)   
	   * JRScalaPlayground (TODO)
	   * Git Local Working Sets (TODO)
	   * JUnit4 Test Suite Generator (TODO)
	   * Cataquavice (TODO)
	   * 3RAD (TODO)
	 * Xtext Runtimes
           * Xtext Runtime 2.7](http://www.eclipse.org/Xtext/) [oomph.setup](https://raw.githubusercontent.com/joergreichert/oomph-catalogue/master/setups/xtextRuntime273.setup)   
           * [Xtext Runtime 2.8](http://www.eclipse.org/Xtext/) [oomph.setup](https://raw.githubusercontent.com/joergreichert/oomph-catalogue/master/setups/xtextRuntime280.setup)   
	   * Xtext Runtime 2.8
	 * General
           * [Oomph Authoring](http://projects.eclipse.org/projects/tools.oomph) [oomph.setup](https://raw.githubusercontent.com/joergreichert/oomph-catalogue/master/setups/OomphAuthoring.setup)   
	   * Oomph Authoring
   * Double click on "Oomph Authoring"
   * leave Stream to "master"
 * page 3
   * Show all variables (Check)
   * Installation location rule: 
     * Select "Installed in a uniquely-named folder within the root install folder
     * ${install.root/}${installation.id}
   * Installation folder name: OomphAuthoring
   * Root install folder: C:\eclipse
   * Workspace location rule: 
     * Select "Installed in a uniquely-named folder within the root workspace-container folder
     * ${workspace.container.root/}${workspace.id}
   * root workspace-container folder: C:\_workspace 
   * Workspace location: oomph_authoring
   * Oomph Authoring Target Platform: Luna
 * page 4
   * Finish
 
## Example for creating a new Oomph setup
### Initial steps
 * use Oomph installer and choose General/Oomph Authoring at the second page to materialize product dedicated for editing setup files
 * create new simple project to be used as container for the setup file to be created
 * File -> New -> Other... -> Oomph/Setup Project Model -> GitHub project
   * Label: Repository Target Generator
   * Name: repository.target.generator
   * Description: Generator for .target and category.xml
   * Git path: joergreichert/RepositoryTargetGenerator
   * Package prefix: de.abg.jreichert.repositorytarget
   * Installable unit id: de.abg.jreichert.repositorytarget.feature.feature.group
   * Installable unit name: de.abg.jreichert.repositorytarget-feature
   * JRE: ${jre.location-1.8}
   * Folder: /de.abg.jreichert.repositorytarget.config.parent
   * Filename: oomph.setup
 
### General hints
 * create new tasks by context menu at project folder (in example: Repository target generator)
 * use compound tasks to group tasks semantically together
 * use context menu: Show properties view to show properties for current task / configuration node
 * use existings setups as template for your own setups, e.g. their preferences configurations
 * you can open an existing setup file, drag the editor to right to share the editor pane with your 
   setup file in the other editor and then move things by drag and drop from the existing setup file
   to your setup file and adapt the items to your needs
 * in the properties view there is a button in the panel at the upper right where you can switch on
   the advanced properties - for some tasks this will show extra options like 
   * trigger: STARTUP, MANUAL, STARTUP+MANUAL
   * explicit configuration of task predecessors and successors
 * open the outline view for the currently open Oomph setup editor
   * Undeclared variables
     * if you have such an entry, that means you use references to variables in your configuration 
	   either without having them declared explicitely or not matching Oomph predefined variables
	 * you can see in the tree sub nodes where these variables are used   
   * Unresolved variables
     * this lists all variables that will be later queried by the Oomph installer dialog's variables wizard page
	 * you can see in the tree sub nodes where these variables are used
	 * in the example these variables aren't resolved yet
	   * git.clone.rtg.location
	   * installation.location
	   * jre.location-1.8
	   * workspace.location
   * Resolved variables
     * all resolved variables from your System context, Eclipse context and the context of the current Oomph configuration
     * you take this list as reference to reuse the variable ids in your configuration instead of 
	   introducing new variables asking for already know values like e.g. git.user.id
   * you can copy an entry in the outline view and if you paste it in an text editor it will be serialized as XML
 * log file of applied Oomph setup: yourEclipseInstallation/configuration/org.eclipse.oomph.setup/setup.log
 * default task order in workspace:
   * Workspace (not explicitley defined)
   * P2 director
   * Eclipse Ini
   * Resource Creation .settings/org.eclipse.ui.ide.prefs (not explicitley defined)
   * Text Modify configuration:/config.ini (not explicitley defined)
   * Resource Creation .metadata/.plugins/org.eclipse.jdt.ui/dialog_settings.xml
   * Preference
   * Git clone
   * Maven Import
   * Launcher
   * Targlets / Target platform
   * Mylyn Queries
   * Working sets
 * use wildcards to parameterize URLs and versions in P2 task and in Target task and then define variables in the stream sections to bind them stream dependent, so there is no need to duplicate the hole task block
 * [To create an Oomph setup from an existing Eclipse installation](https://www.eclipse.org/forums/index.php/t/959921/)
 * use the Oomph simple mode when you don't want to setup your own Oomph file but reuse one of the existing predefine Eclipse installations - you still benefit from the shared bundle repository

### Start configuration
 * task: Eclipse ini
   * option: -Xmx
   * value: 1024M
   * vm: true
 * task: Eclipse ini
   * option: -Doomph.redirection.repository.target.generator.setup
   * value: =https://raw.githubusercontent.com/joergreichert/RepositoryTargetGenerator/${scope.project.stream.name}/releng/de.abg.jreichert.repositorytarget.config.parent/oomph.setup->${git.clone.rtg.location|uri}/releng/de.abg.jreichert.repositorytarget.config.parent/oomph.setup
   * vm: true
   * Description: redirect changes to Oomph configuration triggered within the Eclipse instance to the setup file within the locally cloned repository, so it can be checked in
 * task: Resource creation
   * description: Initialize JDT's package explorer to show working sets as its root objects
   * content:
	<code>
			<?xml version="1.0" encoding="UTF-8"?>
			<section name="Workbench">
				<section name="org.eclipse.jdt.internal.ui.packageview.PackageExplorerPart">
					<item value="true" key="group_libraries"/>
					<item value="false" key="linkWithEditor"/>
					<item value="2" key="layout"/>
					<item value="2" key="rootMode"/>
					<item value="&lt;?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?&gt;&#x0D;&#x0A;&lt;packageExplorer configured=&quot;true&quot; group_libraries=&quot;1&quot; layout=&quot;2&quot; linkWithEditor=&quot;0&quot; rootMode=&quot;2&quot; sortWorkingSets=&quot;false&quot; workingSetName=&quot;&quot;&gt;&#x0D;&#x0A;&lt;localWorkingSetManager&gt;&#x0D;&#x0A;&lt;workingSet editPageId=&quot;org.eclipse.jdt.internal.ui.OthersWorkingSet&quot; factoryID=&quot;org.eclipse.ui.internal.WorkingSetFactory&quot; id=&quot;1382792884467_1&quot; label=&quot;Other Projects&quot; name=&quot;Other Projects&quot;/&gt;&#x0D;&#x0A;&lt;/localWorkingSetManager&gt;&#x0D;&#x0A;&lt;activeWorkingSet workingSetName=&quot;Other Projects&quot;/&gt;&#x0D;&#x0A;&lt;allWorkingSets workingSetName=&quot;Other Projects&quot;/&gt;&#x0D;&#x0A;&lt;/packageExplorer&gt;" key="memento"/>
				</section>
			</section>
   </code>
   * target URL: ${workspace.location|uri}/.metadata/.plugins/org.eclipse.jdt.ui/dialog_settings.xml
   * encoding: UTF-8

### Compile configuration
 * task: variable
   * Type: String
   * Name: eclipse.target.platform
   * Value: Luna
     * this value is used later in the Targlet task to join one of the repository lists matching that name
	 * if you leave off this variable here, the installer will ask you to select a target platform out of Luna, Mars, ...
   * Storage URI: scope://
 * task: JRE
   * Version: JavaSE-1.8
   * Location: ${jre.location-1.8}
 
### IDE features and plug-ins selection
 * selection of installable units to be installed in the IDE to provide required UI features
 * task: P2 directory
   * task: repository
     * URL: http://download.eclipse.org/eclipse/updates/4.4
	 * type: Combined
	 * context menu: Explore
	   * opens repository explorer, where the P2 repository is explored and all contained (in my case this process never stops)
   * task: requirement
 
### IDE preferences
 * usually a good idea to copy this over from one of the existings Oomph setups, e.g. from org.eclipse.oomph/setups/interim/CodeRecommenders.setup
   and then add/adapt/delete preferences as required
 * task: Preference
   * key: /instance/org.eclipse.core.resources/encoding
   * value: UTF-8
 * to capture preference key-value pairs you can also open Window -> Preferences, make changes to the configuration and as soon as 
   you close the preference dialog it is asked to store the changes as Preference tasks - note this works only from the current 
   Eclipse instance running to its local Oomph setup file it was once created from

### Git clone
 * task: Git clone
   * ID: git.clone.rtg
   * Description: Repository Target Generator git repository
     * this property have to be set, as otherwise it will appear later as property to be filled in the installer dialog's variables wizard page
   * Remote name: origin
   * Remote URI: https://github.com/joergreichert/RepositoryTargetGenerator.git
   * Checkout branch: ${scope.project.stream.name}
     * this references the name of the then selected stream at the installer dialog's projects wizard page
 * remark: Oomph setup file wizard and the selection GitHub project generates a Git clone task of that format
   * Remote URI: joergreichert/RepositoryTargetGenerator
   * Annotation, source: http://www.eclipse.org/oomph/setup/InducedChoices
     * inherit = github.remoteURIs
	 * label = ${scope.project.label} Github repository
	 * target = remoteURI
   * later at the installer dialog's variables wizard page you get a selection of different Git URL formats
     * git:/ with authentication
     * https:/ with authentication and github.user.id as part of the Git URL (doesn't work for me as my user name contains an at-sign, but
	   the at-sign is also used to separate user name and actual Git URL)
	 * http:/ anonymous without authentication
   * the installer dialog's variables wizard page also asks you for the password but when then doing the actual Git clone
     the password is rejected because its not in the expected binary format   
   * so in the end I stick to the approach to give the complete GitHub repository URL as described above
 * authentication
   * best to enable authentication outside of Oomph via SSH and git credential store

### Projects Import
 * as with M2E Maven/Tycho support is installed in IDE you can import all projects containing a pom.xml as Maven-enabled projects
 * task: Maven Import
   * create sub node task: Source locator: ${git.clone.rtg.location}
     * git.clone.rtg.location is listed as unresolved variables but actually git.clone.rtg is defined and references the
	   Git clone task above and location is a property of that task (leave empty at the Git clone task declaration) and will
	   be filled later by the Git clone location rule (and as we will use it git.container.root is only variable we have to
	   provide a value for)
 * task: Project Import
   * create sub node task: Source locator: ${git.clone.rtg.location}
   * this additionally imports all non-Maven projects

### Launcher
 * as RepositoryTargetGenerator defines a Xtext DSL and generated sources aren't under version control we have to execute
   the MWE2 grammar workflow to generate the artefacts - for this the pregenerated Eclipse launch configuration can be used
 * task: Launcher
   * launcher: Generate Language Infrastructure (de.abg.jreichert.repositorytarget.dsl)
     * the string for "launcher" have to match the launcher configuration name as listed in the Run -> Run configurations... dialog

### Targlets / Target platform
 * you can use either reuse your existing .target file (option 1) to be set as target platform
   or you define Targlet tasks (option 2)
 * option 1: task: Target Platform
   * Name: Repository Target Generator - Eclipse 4.4.1, Xtext/Xtend 2.7.3
     * this property have to match the name property as used in the target file (as visible workspace-wide when then project
	   containing that target file has been imported as Eclipse project into the workspace)
 * option 2: task: Targlets
   * Oomph setup file wizard and the selection GitHub project generates already a Targlets task of that format
     * task: Targlet
	   * name: ${scope.project.label}
	   * Active Repository List Name: ${eclipse.target.platform}
	   * Include sources: true
	   * Include All Platforms: false
	   * task: Requirement
	     * name: de.abg.jreichert.repositorytarget.feature.feature.group
		 * ...
	   * task: Requirement
	     * name: org.eclipse.sdk.feature.group
		 * ...
	   * Source locator: ${git.clone.location}
	   * task: Repository List, name: Luna
	     * task: Repository
		   * URL: http://download.eclipse.org/releases/luna
		   * Type: Combined
   * the Repository List name is the reference point used by the eclipse.target.platform property,
     we set this property already to value Luna, so the install dialog doesn't show a selection of
	 the target platform
   * the Repository List should contain all respository URLs that are required to resolve the 
     target platform
   * you can use context menu Explore at a Repository List entry to show its contents in the 
     Eclipse view Repository Explorer (analoguous as described under P2 directory task) and then
	 drag and drop plug-ins and features as Requirement - with the C-icon in the toolbar of the 
	 Repository Explorer view you can display all installable units with their fully qualified name
   * when editing a Requirement's name and adding .feature.group the property feature is automatically
     set to true
   * with the annoation as shown below, you can even generate the .target file, that is then used 
     within the Maven build
   * for the example I used the following configuration
     * Annotation, source: http:/www.eclipse.org/oomph/targlets/TargetDefinitionGenerator
	   * location: ${git.clone.rtg.location/releng/de.abg.jreichert.repositorytarget.targetplatform/de.abg.jreichert.repositorytarget.targetplatform.target}
	   * includeAllPlatforms: false
	   * includeSource: false
	   * generateVersions: true
     * Requirements
	   * name="org.eclipse.platform.feature.group
	   * name="org.eclipse.jdt.feature.group"
       * name="org.eclipse.emf.sdk.feature.group"
       * name="org.eclipse.xtext.redist.feature.group, versionRange="[2.7.3,2.8.0)"
       * name="org.eclipse.xtext.ui.feature.group", versionRange="[2.7.3,2.8.0)"
       * name="org.eclipse.xtend.lib", versionRange="[2.7.3,2.8.0)"
       * name="org.eclipse.xtext.xbase.lib, versionRange="[2.7.3,2.8.0)"
     * SourceLocator: rootFolder="${git.clone.rtg.location}", locateNestedProjects="true"
	 * RepositoryList, name="Luna"
       * url="http://download.eclipse.org/releases/luna"
       * url="http://download.eclipse.org/eclipse/updates/4.4"
       * url="http://download.eclipse.org/modeling/emf/emf/updates/releases/"
       * url="http://download.eclipse.org/modeling/tmf/xtext/updates/composite/releases/"
       * url="http://download.itemis.com/updates/releases/2.1.1/"
       * url="http://www.xpect-tests.org/updatesite/nightly/"

### Working sets
 * working sets can be set up by e.g. applying path matching patterns, so as the Git
   repository folder structure already reflects the different types of projects, it
   can be reused for the working sets
 * task: Working Sets
   * task: Working Set, name="Release Engineering"
     * LocationPredicate: pattern=".*/releng/.*"
   * task: Working Set, name="Plug-ins"
     * LocationPredicate: pattern=".*/plugins/.*"
   * task: Working Set, name="Tests"
     * LocationPredicate: pattern=".*/tests/.*"
   * task: Working Set, name="Examples"
     * LocationPredicate: pattern=".*/releng/.*"
   * task: Working Set, name="Update Site"
     * LocationPredicate: pattern=".*/features/.*"

### Mylyn
 * you can set up Mylyn task repositories and issue queries
 * task: Variable:
   * type: PASSWORD
   * name: github.user.password
   * label: GitHub password for issues
 * task: Mylyn Queries
   * connectorKind: github
   * repositoryURL: https://github.com/joergreichert/RepositoryTargetGenerator
   * userID: ${github.user.id}
   * password: ${github.user.password}
   * task: Query
     * summary: ${scope.project.label} bugs
	 * Query attribute (key: state, value: open::)
	 * Query attribute (key: labels, value: bug::)
   * task: Query
     * summary: ${scope.project.label} features
	 * Query attribute (key: state, value: open::)
	 * Query attribute (key: labels, value: enhancement::)
   * task: Query
     * summary: ${scope.project.label} resolved
	 * Query attribute (key: state, value: closed::)
 * a Mylyn Queries with connectorKind "githubPullRequests" can be used to
   query pull requests
 * with task "Mylyn Builds" and connector kind "org.eclipse.mylyn.hudson"
   you can query Jenkins server status
	 
### Streams
 * typically reflecting branches or tags in the GitHub repository
 * in example
   * task: Stream: name=master"
   * task: Stream: name="release"
 * if you have special configuration for the streams you can
   create tasks as sub nodes as you have done under the project
   node
   
### Tasks not used yet in this example
 * Redirection
   * redirects a source URL to a target URL
 * API base line
   * Preferences -> Plug-in Development/API base lines entries
 * File Associations
   * Preferences -> General/Editors/File Associations entries
 * Key bindings
   * Preferences -> General/Keys entries
 * Link location
   * Reference external P2 repository location
 * Path variable
   * Preferences -> Java/Build Path/Classpath Variables
 * Path variable
   * Preferences -> Java/Build Path/Classpath Variables
 * Project Set Import
   * URL pointing to *.psf file (project team set definition)
 * Resource copy   
   * copy an artifact identified by source URL to a target URL
 * String Substitution  
   * replace a wildcard or variable (e.g from the environment) with a value 
 * Text Modifiy (used e.g. for eclipse.ini)
 * Annotation
   * additional data to break out of the structure of the meta model
     (implies knowledge about internal implementation of task and its
     hidden configuration parameters)	 

## Example for executing Oomph setup
### Product
 * hit the refresh button (to load propably updated product configuration)
 * Eclipse Standard/SDK
 * Product version: Latest release (Luna)
 * Bundle pool (check): C:\_oomph_bundle_pool
 * Check if the Update Button is enabled, if yes, install the latest Oomph version, before you continue
### Projects
 * hit the refresh button (to load propably updated project configuration)
 * Joerg-Projects/Joerg's GitHub projects/Repository target generator -> Double click
 * stream: release
### Variables
 * Installation location rule: ${install.root/}${installation.id}
 * Installation folder name: RepositoryTargetGeneratorDev
 * Workspace location rule: ${workspace.container.root/}${workspace.id}
 * Workspace folder name: repository_target_generator_dev
 * Root workspace-container folder: C:\_workspaces
 * Git clone location rule: ${git.container.root/}${@id.remoteURI|gitRepository/}${@id.checkoutBranch}
 * Root Git-container folder: C:\git
 * GitHub password for issues: ...
 * JRE 1.8 Location: C:\ProgramData\Java\JDK8
 * git.clone.rtg.description: bla
 * GitHub user ID: de.abg.reichert.joerg@googlemail.com
### Confirmation
 * Mirrors (Checked)
 * Offline (only check, if all P2 artefacts have been downloaded in previous sessions)
 * Override (only check, if you want to override an existing installation)
### In installed IDE
 * close Welcome page
 * confirm "Do you agree to download it (size 1MB) from 'http://download.itemis.com/antlr-generator-3.2.0-patch.jar'?" with y and Enter
 * Check if the circle arrow symbol in the bottom status bar has no error marker (you can click on it to see the current setup status)
 * if dialog pops up with requesting eclipse.exe to pass firewall, confirm
 * With Help -> Perform Setup Tasks... you can manually trigger the setup tasks again

## Resources 
 * [Original project proposal](https://projects.eclipse.org/proposals/oomph) 
 * [Official homepage](https://projects.eclipse.org/projects/tools.oomph) 
 * [Oomph Help Center](http://download.eclipse.org/oomph/help/) 
 * [Eclipse Oomph Installer Help](http://git.eclipse.org/c/cdo/cdo.git/plain/plugins/org.eclipse.emf.cdo.releng.setup/help/installer/index.html) 
 * [Eclipse Oomph Installer](https://wiki.eclipse.org/Eclipse_Oomph_Installer) 
 * [Eclipse Oomph Authoring](https://wiki.eclipse.org/Eclipse_Oomph_Authoring) 
 * [Quicker start guide for Oomph](https://blogs.itemis.de/leipzig/archives/936) 
 * [Creating custom installations with Oomph](http://www.winklerweb.net/index.php/blog/12-eclipse/20-creating-custom-installations-with-oomph) 
 * [Eclipse has Oomph](http://www.eclipse.org/community/eclipse_newsletter/2014/may/article3.php) 
 * [Oomph: A Matter of Preference](http://www.eclipse.org/community/eclipse_newsletter/2014/november/article2.php) 
 * [Oomph: Automatically Provision a Project-specific IDE (XtextCON)](http://vimeo.com/98438046) 
 * [Oomph: Automatically Provision a Project-specific IDE](https://www.youtube.com/watch?v=_QlSosecEUo) 
 * [Redirecting Oomph Product and Project Catalogs](https://blogs.itemis.de/leipzig/archives/951) 
 * [Oomph Eclipse Forum](http://www.eclipse.org/forums/index.php?t=thread&frm_id=287) 
 * [Oomph Contribution Guide](http://wiki.eclipse.org/Oomph_Contribution_Guide) 
 * [Shoes for the Shoemaker](http://ed-merks.blogspot.de/2014/02/shoes-for-shoemaker.html) 

## Example status
### C:\Users\Reichert\.p2
#### pools.info

```	   
        C:\Users\Reichert\.p2\pool
```

#### profiles.info

```
        <empty>
```

### C:\_oomph_agent
#### pools.info
	 
```
	    C:\_oomph_bundle_pool
```

#### profiles.info
	 
```
  	    C__eclipse_OomphAuthoring_eclipse|Installation|C:\\_oomph_bundle_pool|C:\\eclipse\\OomphAuthoring\\eclipse|
```

### C:\Users\Reichert\.eclipse\org.eclipse.oomph.p2
#### agents.info
	 
```
  	      C:\Users\Reichert\.p2
          C:\_oomph_agent
```

#### defaults.info
	 
```
          org.eclipse.oomph.setup.ui=C\:\\_oomph_bundle_pool
```

### C:\Users\Reichert\.eclipse\org.eclipse.oomph.p2\setups
#### catalogs.setup
	 
```
<?xml version="1.0" encoding="UTF-8"?>
<setup:CatalogSelection
    xmi:version="2.0"
    xmlns:xmi="http://www.omg.org/XMI"
    xmlns:setup="http://www.eclipse.org/oomph/setup/1.0">
  <productCatalog
      href="index:/org.eclipse.setup#//@productCatalogs[name='org.eclipse.products']"/>
  <projectCatalog
      href="index:/org.eclipse.setup#//@projectCatalogs[name='org.eclipse']"/>
  <defaultProductVersion
      key="index:/org.eclipse.setup#//@productCatalogs[name='org.eclipse.products']/@products[name='epp.package.standard']"
      value="index:/org.eclipse.setup#//@productCatalogs[name='org.eclipse.products']/@products[name='epp.package.standard']/@versions[name='latest.released']"/>
  <defaultStream
      key="index:/org.eclipse.setup#//@projectCatalogs[name='org.eclipse']/@projects[name='XtextContainer']/@projects[name='Oomph%20Authoring']"
      value="index:/org.eclipse.setup#//@projectCatalogs[name='org.eclipse']/@projects[name='XtextContainer']/@projects[name='Oomph%20Authoring']/@streams[name='master']"
      selection="true"/>
</setup:CatalogSelection>	 
```

#### locations.setup
	 
```
<?xml version="1.0" encoding="UTF-8"?>
<setup:LocationCatalog
    xmi:version="2.0"
    xmlns:xmi="http://www.omg.org/XMI"
    xmlns:setup="http://www.eclipse.org/oomph/setup/1.0">
  <installation>
    <key href="file:/C:/eclipse/OomphAuthoring/eclipse/configuration/org.eclipse.oomph.setup/installation.setup#/"/>
    <value href="file:/C:/_workspaces/oomph_authoring/.metadata/.plugins/org.eclipse.oomph.setup/workspace.setup#/"/>
  </installation>
  <workspace>
    <key href="file:/C:/_workspaces/oomph_authoring/.metadata/.plugins/org.eclipse.oomph.setup/workspace.setup#/"/>
    <value href="file:/C:/eclipse/OomphAuthoring/eclipse/configuration/org.eclipse.oomph.setup/installation.setup#/"/>
  </workspace>
</setup:LocationCatalog>
```

#### user.setup
	 
```
<?xml version="1.0" encoding="UTF-8"?>
<setup:User
    xmi:version="2.0"
    xmlns:xmi="http://www.omg.org/XMI"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:setup="http://www.eclipse.org/oomph/setup/1.0"
    name="Reichert"
    unsignedPolicy="ACCEPT"
    questionnaireDate="2014-12-21T10:23:48.190+0100">
  <setupTask
      xsi:type="setup:CompoundTask"
      name="User Preferences">
    <annotation
        source="http://www.eclipse.org/oomph/setup/UserPreferences">
      <detail
          key="/instance/org.eclipse.jdt.launching/org.eclipse.jdt.launching.PREF_DEFAULT_ENVIRONMENTS_XML">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.linuxtools.rpm.ui.editor/rpmLisMastBuild">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.jdt.core/org.eclipse.jdt.core.classpathVariable.JRE_SRCROOT">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.search/org.eclipse.search.defaultPerspective">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/workspace_target_handle">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.mylyn.team.ui/org.eclipse.mylyn.team.commit.template">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.jdt.core/org.eclipse.jdt.core.classpathVariable.JRE_SRC">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.jdt.launching/org.eclipse.jdt.launching.PREF_VM_XML">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.mylyn.tasks.ui/org.eclipse.mylyn.data.dir">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.ui.ide/WORKSPACE_NAME">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.jdt.core/org.eclipse.jdt.core.classpathVariable.JRE_LIB">
        <value>ignore</value>
      </detail>
      <detail
          key="/instance/org.eclipse.core.resources/encoding">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.ui.editors/spellingEnabled">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.ui.workbench/RUN_IN_BACKGROUND">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.core.resources/refresh.lightweight.enabled">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.ui.editors/lineNumberRuler">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/target_platform_realization">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/checkedVersionPlugins">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/pooled_urls">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.os">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/program_args">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/vm_launcher_ini">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/implicit_dependencies">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/target_mode">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.arch">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/additional_locations">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.ws">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/external_features">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.nl">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.jdt.core/org.eclipse.jdt.core.classpathVariable.ECLIPSE_HOME">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/checkedPlugins">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/pooled_bundles">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/vm_args">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.pde.core/target.profile">
        <value>record</value>
      </detail>
      <detail
          key="/instance/org.eclipse.core.runtime/line.separator">
        <value>record</value>
      </detail>
    </annotation>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.core.resources">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.core.resources/encoding"
          value="UTF-8"/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.core.resources/refresh.lightweight.enabled"
          value="true"/>
    </setupTask>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.core.runtime">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.core.runtime/line.separator"
          value="&#xA;"/>
    </setupTask>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.jdt.core">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.jdt.core/org.eclipse.jdt.core.classpathVariable.ECLIPSE_HOME"
          value="C:/git/RepositoryTargetGenerator/releng/de.abg.jreichert.repositorytarget.repository/target/repository"/>
    </setupTask>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.pde.core">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/additional_locations"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/checkedPlugins"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/checkedVersionPlugins"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/external_features"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/implicit_dependencies"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.arch"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.nl"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.os"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/org.eclipse.pde.ui.ws"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/pooled_bundles"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/pooled_urls"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/program_args"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/target.profile"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/target_mode"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/target_platform_realization"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/vm_args"
          value=""/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.pde.core/vm_launcher_ini"
          value=""/>
    </setupTask>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.ui.editors">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.ui.editors/lineNumberRuler"
          value="true"/>
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.ui.editors/spellingEnabled"
          value="true"/>
    </setupTask>
    <setupTask
        xsi:type="setup:CompoundTask"
        name="org.eclipse.ui.workbench">
      <setupTask
          xsi:type="setup:PreferenceTask"
          key="/instance/org.eclipse.ui.workbench/RUN_IN_BACKGROUND"
          value="true"/>
    </setupTask>
  </setupTask>
  <setupTask
      xsi:type="setup:VariableTask"
      type="FOLDER"
      name="install.root"
      value="C:\eclipse"
      label="Root install folder">
    <description>The root install folder where all the products are installed</description>
  </setupTask>
  <setupTask
      xsi:type="setup:VariableTask"
      type="FOLDER"
      name="workspace.container.root"
      value="C:\workspace"
      label="Root workspace-container folder">
    <description>The root workspace-container folder where all the workspaces are located</description>
  </setupTask>
  <attributeRule
      attributeURI="http://www.eclipse.org/oomph/setup/1.0#//InstallationTask/location"
      value="${install.root/}${installation.id}"/>
  <attributeRule
      attributeURI="http://www.eclipse.org/oomph/setup/1.0#//WorkspaceTask/location"
      value="${workspace.container.root/}${workspace.id}"/>
  <acceptedLicense>6a3d083ad2bd7d3a80ee293235f8c5b1 Eclipse Foundation Software User Agreement</acceptedLicense>
</setup:User>
```
 
