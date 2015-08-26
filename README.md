# Node Application Metrics Dashboard

A data visualizer that uses "[ Node Application Metrics][1]" (appmetrics) to monitor and display Node.js application data as a html web application.

### Prerequisites
The Node Application Metrics Dashboard supports all versions of Node.js and io.js supported by 'appmetrics'.

### Configuration

In order to configure an application to be monitored by appmetrics-dash, the following line of code must be added to the application. 

```sh
var app = require('appmetrics-dash').start(config);  
```
Where the optional `config` parameter is an options hash as follows:
* `server`: A pre-existing http server to use. If not specified one is created.
* `port`: The port to use if creating a http server, with `default: 3000` 
* `url`: The url for the dashboard, with `default: /admin`
* `uid`: The User ID used to log into the dashboard, with `default: 'admin'`
* `password`: The password used to log into the dashboard, with `default 'admin'`

This line will do one of 2 things, depending on the monitored application:

1.  If no config is provided, or no server is specified in the config, appmetrics-dash will create its own HTTP server (default port 3000).
2.    If a server is provided in the config, appmetrics-dash will reuse that server.

### Data Visualisation

The data from Node Applicaiton Metrics is visualized in the browser using the following steps:
1. Run the application you wish to monitor.
2. Connect to your application via a web browser (default port 3000).
3. Add the dashboard URL (default '/admin') to the end of the address of the connected application and input the id and password (default: 'admin', 'admin') when prompted.
4. A set of visual representations such as charts will display realtime and historical data (cpu usage, memory usage and garbage collection data) that has been generated by the application.
5. You can then select and deselect certain types of information using the Options Menu and clicking Display Selected Information to update the display.

### License
The Node Application Metrics Dashboard is licensed using an Apache v2.0 License.

[1]:https://developer.ibm.com/open/node-application-metrics/ 