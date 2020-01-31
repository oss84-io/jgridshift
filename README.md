

## Release Notes

### jGridShift 1.3

- Moved package `au.com.objectix.jgridshift.jca` from the core jar file to a jca module.
  Its accidental inclusion in core resulted in an undesired dependency on an old JavaEE API.
- Restored code examples in the sample module.

### jGridShift 1.2

_TODO_

### jGridShift 1.0

This release contains no significant changes to the core API.
A J2EE JCA adapter has been added, along with a web service sample app.

The contents are:
- an API only jar
- a JCA adapter rar with a sample service descriptor for JBoss
- a J2EE ear including a sample deployment descriptor for JBoss
- a GUI sample tool packaged in an executable jar.
- full source
- core API, JCA and samples released under the GNU
Lesser General Public License.

The API jar can used in any application and has no dependencies.

The GUI tool is a Swing app and the executable jar contains all the classes
needed. Just run the jar and tell it where your grid shift binary is
(refer to http://jgridshift.sourceforge.net for info on where to get
gridshift binaries).

The JCA adapter contains the resource adapter xml, but needs a service
descriptor to be deployable. A sample for JBoss is included. Just edit
the jgridshift-service.xml to identify where your gridshift binary is,
drop the xml file and the jgridshift.rar into your deployment directory
and away you go. Refer to the SessionBean sample for how you acquire
and use a JCA connection.

The web service sample is pretty specific to JBoss. It requires JBoss-Net,
which is not part of the default server (in 3.2 at least). The easiest
option is to make the full server the default. The JCA adapter must be
deployed, then just drop the ear into your deployment directory.
