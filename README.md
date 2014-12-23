oomph-catalogue
===============

Custom product and project catalogue for my GitHub projects, inspired by [Alex' oomph setups](https://github.com/nittka/oomph-playground).

## Setup

 * download the [Oomph installer](http://wiki.eclipse.org/Eclipse_Oomph_Installer) 
 * add the following line to the installer's oomph.ini

`-Doomph.redirection.setups=http://git.eclipse.org/c/oomph/org.eclipse.oomph.git/plain/setups/->https://raw.githubusercontent.com/joergreichert/oomph-catalogue/master/setups/`

 * start the Oomph installer
 
## Example walkthrough
 * 1.0.0 Build 715
 * page 1
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
	   * ActiveAnnotationsExamples: BeanFX (TODO)
	   * ActiveAnnotationsExamples: JPA (TODO)
	   * ActiveAnnotationsExamples: NLS (TODO)
	   * ActiveAnnotationsExamples: StopWatch (TODO)
	   * ActiveAnnotationsExamples: TestSuite (TODO)
	   * RepositoryTargetGenerator (TODO)
	   * mobilecloud-14-xtend (TODO)
	   * OperaMisterWongBookmarks (TODO)
	   * OperationsResearch (TODO)
	   * XtextPlayground (TODO)
	   * Permet (TODO)
	   * Cool (TODO)
	   * Spray (TODO)
	   * JRScalaPlayground (TODO)
	   * Git Local Working Sets (TODO)
	   * JUnit4 Test Suite Generator (TODO)
	   * Cataquavice (TODO)
	   * 3RAD (TODO)
	 * Xtext Runtimes
	   * Xtext Runtime 2.7
	 * Android Runtimes (TODO)
	 * Spring / Gradle Runtime (TODO)
	 * Scala Runtime (TODO)
	 * Oomph Authoring (TODO)
   * Double click on "Xtext Runtime 2.7"
   * leave Stream to "master"
 * page 3
   * Show all variables (Check)
   * Installation location rule: 
     * Select "Installed in a uniquely-named folder within the root install folder
     * ${install.root/}${installation.id}
   * Installation folder name: EclipseLuna
   * Root install folder: C:\eclipse
   * Workspace location rule: 
     * Select "Installed in a uniquely-named folder within the root workspace-container folder
     * ${workspace.container.root/}${workspace.id}
   * root workspace-container folder: C:\_workspace 
   * Workspace location: eclipse44
   * Xtext Runtime 2.7 Target Platform: Luna
 * page 4
   * Finish
   
   
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
  	    C__eclipse_EclipseLuna_eclipse|Installation|C:\\_oomph_bundle_pool|C:\\eclipse\\EclipseLuna\\eclipse|
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
      key="index:/org.eclipse.setup#//@projectCatalogs[name='org.eclipse']/@projects[name='XtextContainer']/@projects[name='Xtext%20Runtime%202.7']"
      value="index:/org.eclipse.setup#//@projectCatalogs[name='org.eclipse']/@projects[name='XtextContainer']/@projects[name='Xtext%20Runtime%202.7']/@streams[name='master']"
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
    <key href="file:/C:/eclipse/EclipseLuna/eclipse/configuration/org.eclipse.oomph.setup/installation.setup#/"/>
    <value href="file:/C:/_workspaces/eclipse_luna/.metadata/.plugins/org.eclipse.oomph.setup/workspace.setup#/"/>
  </installation>
  <workspace>
    <key href="file:/C:/_workspaces/eclipse_luna/.metadata/.plugins/org.eclipse.oomph.setup/workspace.setup#/"/>
    <value href="file:/C:/eclipse/EclipseLuna/eclipse/configuration/org.eclipse.oomph.setup/installation.setup#/"/>
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
 * to be continued
 
### General hints
 * create new tasks by context menu at project folder (in example: Repository target generator)
 * use compound tasks to group tasks semantically together
 * use context menu: Show properties view to show properties for current task / configuration node
 * use existings setups as template for your own setups, e.g. their preferences configurations
 * you can open an existing setup file, drag the editor to right to share the editor pane with your 
   setup file in the other editor and then move things by drag and drop from the existing setup file
   to your setup file and adapt the items to your needs

### Start configuration
 * task: Eclipse ini
   * option: -Xmx
   * value: 1024M
   * vm: true
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
   * Value: None
   * Storage URI: scope://
 * task: JRE
   * Version: JavaSE-1.8
   * Location: ${jre.location-1.8}
 
### IDE features and plug-ins selection
 * task: P2 directory
   * task: repository
     * URL: http://download.eclipse.org/eclipse/updates/4.4
	 * type: Combined
	 * context menu: Explore
	   * opens repository explorer, where the P2 repository is explored and all contained (in my case this process never stops)
   * task: requirement
 
### IDE preferences

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
 