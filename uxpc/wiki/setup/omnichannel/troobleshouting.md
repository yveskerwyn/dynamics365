# Troubleshooting

See blogpost about the solution I also got from Microsoft here below: https://www.victorsolaya.com/blog/omnichannel-error-in-wave-2/

## Check if the Omnichannel Channel Provider is on the org

Go to <orgUrl>/main.aspx?forceUCI=1&pagetype=entitylist&etn=msdyn_ciprovider

-> https://m3l-ce.crm4.dynamics.com/main.aspx?forceUCI=1&pagetype=entitylist&etn=msdyn_ciprovider

## Get the cdnUrl

<orgUrl>/api/data/v9.1/serviceendpoints(38bd8b51-de34-4c45-bf43-5a913aeec49f)?$select=path

https://m3l-ce.crm4.dynamics.com/api/data/v9.1/serviceendpoints(38bd8b51-de34-4c45-bf43-5a913aeec49f)?$select=path



{"@odata.context":"https://m3l-ce.crm4.dynamics.com/api/data/v9.1/$metadata#serviceendpoints(path)/$entity","path":"https://oc-cdn-public-eur.azureedge.net/","serviceendpointid":"38bd8b51-de34-4c45-bf43-5a913aeec49f","_organizationid_value":"866bb1f8-324e-4bf2-a179-a3a5c124e87c"}

cdnUrl = https://oc-cdn-public-eur.azureedge.net/ ?


## Get the ocUrl

<orgUrl>/api/data/v9.1/serviceendpoints(8af92c33-e748-4b5a-b772-46cba89bb7ac)?$select=path

https://m3l-ce.crm4.dynamics.com/api/data/v9.1/serviceendpoints(8af92c33-e748-4b5a-b772-46cba89bb7ac)?$select=path

{"@odata.context":"https://m3l-ce.crm4.dynamics.com/api/data/v9.1/$metadata#serviceendpoints(path)/$entity","path":"https://720678702d07456899a84f02ad8522-crm4.omnichannelengagementhub.com","serviceendpointid":"8af92c33-e748-4b5a-b772-46cba89bb7ac","_organizationid_value":"866bb1f8-324e-4bf2-a179-a3a5c124e87c"}

ocUrl = https://720678702d07456899a84f02ad8522-crm4.omnichannelengagementhub.com ?

## Add a new Channel Provider

Channel Url: <cdnUrl>/convcontrol/ChatControl.htm?uci=true&clientName=zfp&cloudType=Public&env=prod&ocBaseUrl=<ocUrl>&ucilib=<orgUrl>/webresources/Widget/msdyn_ciLibrary.js


Ontleed:

- <cdnUrl> https://oc-cdn-public-eur.azureedge.net

- /convcontrol/ChatControl.htm?uci=true&clientName=zfp&cloudType=Public&env=prod&ocBaseUrl=

- <ocUrl> https://720678702d07456899a84f02ad8522-crm4.omnichannelengagementhub.com

- &ucilib=

- <orgUrl> https://m3l-ce.crm4.dynamics.com

- /webresources/Widget/msdyn_ciLibrary.js


https://oc-cdn-public-eur.azureedge.net/convcontrol/ChatControl.htm?uci=true&clientName=zfp&cloudType=Public&env=prod&ocBaseUrl=https://720678702d07456899a84f02ad8522-crm4.omnichannelengagementhub.com&ucilib=https://m3l-ce.crm4.dynamics.com/webresources/Widget/msdyn_ciLibrary.js


Orginal value:

https://oc-cdn-public-eur.azureedge.net/convcontrol/ChatControl.htm?uci=true&clientName=zfp&cloudType=Public&env=prod&ocBaseUrl=https://720678702d07456899a84f02ad8522-crm4.omnichannelengagementhub.com&ucilib=https://m3l-ce.crm4.dynamics.com/webresources/Widget/msdyn_ciLibrary.js