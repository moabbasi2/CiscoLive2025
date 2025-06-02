**Cumulus Insurance - Use Case 1** (Cumulus Insurance - Demo1.zip) - Download and extract all the three files.

Go to the AI Agent Studio and import both AI Agents configs (**+Suggested Response AI Agent.json** & **Cumulus Insurance AI Agent.json**) individually. 
Verify data is present, then Click Save > Publish.

Import '**CumulusInsurance_LiveChat_v33.workflow**' to your Webex Connect service and make the following changes:
- Open Node number 2436 and 2438 and set to your Form Template (make sure you have atleast Email as one of the form field)
- Open all the Receive Nodes, and click Save.
- Open Suggested Response node, and select your +Suggested Response AI agent (published in Step-1).
- Open AI Agent node, and select your Cumulus Insurance AI agent (published in Step-2).
- Open Queue Task node, and select your LiveChat queue.
- Go to Flow Settings > Custom Variables > Change the following fields according to your tenant:
  a) appId
  b) liveChatDomain
  c) queueId
  d) Optional - If you do not have JourneyID integration - ignore 'iframeId' and 'iframeSecret'
