Front end
aded zip file into the dropins directory of your eclipse
   installation.

2. Enable Custom GWT Checkstyle checks:

Copy "settings/code-style/gwt-customchecks.jar" into:
  <eclipse>/plugins/com.atlassw.tools.eclipse.checkstyle_x.x.x/extension-libraries

3. Import GWT Checks:

Window->Preferences->Checkstyle->New...
Set the Type to "External Configuration File"
Set the Name to "GWT Checks" (important)
Set the location to "settings/code-style/gwt-checkstyle.xml".
Suggested: Check "Protect Checkstyle configuration file".
Click "Ok".

4. Import GWT Checks for Tests

Repeat step 3, except:
Set the Name to "GWT Checks for Tests" (important)
Set the location to "settings/code-style/gwt-checkstyle-tests.xml".

== Importing the Google Plugin projects ==

Having set up your workspace appropriately, you can now import the appropriate
projects.

File -> Import -> General -> Existing Projects into Workspace

Select your checkout of the trunk of Google Eclipse Plugin to see all of the
Eclipse projects for you to import. You should only import the projects that
correspond to the version of Eclipse that you are using for development, and
the platform you are running on. For example, if you have Eclipse 3.4, do not
import a project that has "3.3" in its name. As another example, if you are
running on Windows, do not import projects that have readme "win32" or "macosx"
in their name. 

== Launching the Plugin ==

Once your projects have been imported, go to the Package Explorer and
right-click on the "com.google.gdt.eclipse.suite" project. Go to 
"Run As" > "Eclipse Application".  Another instance of Eclipse should launch,
running GPE!

Note: Setting these two environment variables will cause the GWT and App Engine
SDKs to be registered as GPE SDK Bundles. However, in development mode, this
only happens when the workbench metadata is first created. To have the workbench
pick up changes to these variables,  go to the Main tab in your launch
configuration, and check 'Clear' under Workspace Data. Note that this will also
remove any projects that you created in the runtime workbench.

