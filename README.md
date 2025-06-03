_Pre-requisite: Webex CC, Webex Connect, AI Autonomous Agent (Beta), Summarize Text Beta node, Journey node (JDS)_


**DEMO-1 Cumulus Insurance - AI Powered LiveChat**
        
        - Download and extract all the files (Demo-1 CumulusInsurance LiveChat.zip)
        
        - Go to the AI Agent Studio and create a KB document for Cumulus Insurance FAQ (for customer interaction) and upload the ‘Cumulus Insurance FAQs.docx’ file to it
        
        - Create another KB document for Suggested Response FAQ (for agent assistance) and upload the ‘Suggested Response FAQ-detailed.docx’ file to it.
        
        - Import the AI Agent for Cumulus Insurance (Cumulus Insurance AI Agent.json) and attach the Cumulus Insurance FAQ Knowledgebase to it. Go to Action tab and make sure ‘Agent handoff tab is enabled’
        
        - Import the AI Agent for Suggested Response (+Suggested Response AI Agent.json) and attach the Suggested Response FAQ Knowledgebase to it. Make sure ‘Agent handoff action is disabled’
        
        - Finally, import the ‘CumulusInsurance_LiveChat_v33’ workflow to your Webex Connect service and publish it to test this use case
        
        * Follow general guidelines to adjust flow and node settings based on your tenant.


**DEMO-2 CumulusAir Proactive Notifications - AMB/Email with AI Powered Voice Channel**

        Proactive Notifications:
        
        - Download and extract all the files (Demo-2 CumulusAir AMBandVoice.zip)
        
        - Import 'CumulusAir-ProactiveNotify.workflow' within your Connect service

        - Make changes to the REST Nodes (Get Passenger Details and Update Booking) according to your external DB/Sheets maintaining customer/bookings/flight details. Within the same nodes, you can create the output variable and parse the value of the required fields. Update all the nodes with the new variable names. Also check the flow settings and save your business email Id. Save and Publish to test using a webhook trigger

        AI Powered Voice flow:
        
        - Go to the AI Agent Studio and create a KB document for CumulusAir FAQ and upload all the 5 FAQ docx files to it
        
        - Import the AI Agent for CumulusAir (CumulusAir_AIAgent.json) and attach the CumulusAir FAQ KB to it. Make sure all action steps are populated. Each actions pointing to the AI Agent Workflows which will be imported and configured in the next couple of steps. Save and Publish the AI Agent.
        
        - Import the ‘GetBookingAIWorkflow’ and 'UpdateBookingAI Workflow' AI workflows to your Webex Connect service and configure the REST nodes according to your DB/Sheet. Important step is to go to workflow settings > Flow Outcomes > Last Execution Status > turn on notify > and set the Key name matching with the AI Agent Action trigger name > pass the Key values returned from the REST payload, AI Agent can read those values to the user. For the pupose of demo, we are sharing just couple of AI Agent workflows, you can build the remaining workflows accoring to your use case.

        - Goto AI agent configuration and make sure to associate your AI agent workflows to the correct Action triggers. Save, Preview and Republish the AI Agent.

        - Go to WxCC Flows and Import Voice flow 'CumulusAir_Voice_AIAgent.json' and select the TTS connector and your AI agent from Virtual Agent V2 node. Publish it and associate it your voice inbound channel/entry point to test the flow.


**DEMO-3 CumulusAir PostFly - AI Powered Email Channel**

        - Import 'CumulusAir-EmailwithAIAgent.workflow' within your Connect service

        - Go to settings and customer variables and change the 'bizemailid' to your business email id (email asset) and queueId (refer to control hub > email queue)

        - Select the 'CumulusAir_AIAgent' from the AI Agent node and configure the remaining nodes as required and publish the flow to test it


All the best !!
