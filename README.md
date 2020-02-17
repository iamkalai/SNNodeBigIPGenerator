**SNNodeBigIPGenerator**
======================

This adds a SN list row context menu that you can use to generate the Big IP for a ServiceNow node.

**Description:**
----------------

ServiceNow does not has any native facility to switch between different nodes of a ServiceNow instance. There are some plugins that you can use to switch between the nodes but I required a native feature that I can use to do the same. This utility uses the base code and derives the idea from [ServiceNow-Utils](https://github.com/arnoudkooi/ServiceNow-Utils). If you wish to use a browser plugin, you should defintely try out ServiceNow-Utils.

For now, this button only generates the ID required to switch between the nodes and does not actually switch between the nodes directly. Follow the steps described in Usage section to know more on how to use this facility to switch between the nodes.

**Installation:**
-----------------

*Install the updateset found in dist folder* - "Get SN Node BigIP.xml" updateset creates the UI context menu and a script include that supports it's operation. All the components that are being created are new and do not change any out of the box settings.

**Usage:**
----------

Once you have installed the updateset,

1. Navigate to 'Node States(sys_cluster_state)' table.
2. Right click on the node you want to switch to and select 'Copy BigIP'. This copies the ID required to switch between the node.

If you are using Chrome browser, follow the below steps.

3. Open Chrome DevTools.
4. Click the Application tab to open the Application panel. The Manifest pane will probably open.
5. Under Storage expand Cookies, then select an origin (containing the ServiceNow instance URL).
6. Find the cookie named "BIGipServerpool_instancename".
7. Replace the cookie value with the value copied from Step-2 using the context menu.
8. Refresh the browser window.

If you are using any other browser, use the utility equivalent to the DevTools from Step-3 to edit the cookie value.

**License:**
------------

GNU General Public License v3.0
