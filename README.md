_Pre-requisite: Webex CC, Webex Connect, AI Autonomous Agent (Beta), Summarize Text Beta node, Journey node (JDS)_


**DEMO-1 Cumulus Insurance - AI Powered LiveChat**
        
        - Download and extract all the files (Demo-1 CumulusInsurance LiveChat.zip)
        
        - Go to the AI Agent Studio and create a Knowledge Base (KB) for Cumulus Insurance FAQ which will be used for customer interaction. 

        - Upload the 'Cumulus Insurance FAQs.docx' file to it.
        
        - Create another KB for Suggested Response FAQ which will be used for agent assistance and upload the 'Suggested Response FAQ-detailed.docx' file to it.
        
        - Import the AI Agent for Cumulus Insurance (Cumulus Insurance AI Agent.json) and map the Cumulus Insurance FAQ Knowledge Base to it. Go to the Action tab and ensure 'Agent handoff' is enabled.
        
        - Import the AI Agent for Suggested Response (+Suggested Response AI Agent.json) and map the Suggested Response FAQ Knowledge Base to it. Make sure 'Agent handoff action' is disabled.
        
        - Finally, import the 'CumulusInsurance_LiveChat_v33' workflow into your Webex Connect service and publish it to test this use case.
        
        - Follow general guidelines to adjust flow and node settings based on your tenant.


**DEMO-2 CumulusAir Proactive Notifications - AMB/Email with AI Powered Voice Channel**

        Proactive Notifications:
        
        - Download and extract all the files (Demo-2 CumulusAir AMBandVoice.zip)
        
        - Import 'CumulusAir-ProactiveNotify.workflow' within your Connect service

        - Make changes to the REST Nodes ('Get Passenger Details' and 'Update Booking') according to your external database/sheets maintaining customer/bookings/flight details. Within the same nodes, you can create the output variable and parse the values of the required fields. Update all nodes with the new variable names. Also, check the flow settings and save your business email ID. Save and publish to test using a webhook trigger.

        AI Powered Voice flow:
        
        - Go to the AI Agent Studio and create a KB for CumulusAir FAQ. Upload all five FAQ .docx files to it.
        
        - Import the AI Agent for CumulusAir (CumulusAir_AIAgent.json) and map the CumulusAir FAQ KB to it. Ensure all action steps are populated, with each action pointing to the AI Agent Workflows that will be imported and configured in the next couple of steps. Save and publish the AI Agent.
        
        - Import the 'GetBookingAIWorkflow' and 'UpdateBookingAI Workflow' AI workflows into your Webex Connect service and configure the REST nodes according to your database/sheet. 
	
        - An important step is to go to workflow settings > Flow Outcomes > Last Execution Status > turn on notify > and set the Key name matching the AI Agent Action trigger name > pass the Key values returned from the REST payload; the AI Agent can read those values to the user. For the purpose of the demo, we are sharing just a couple of AI Agent workflows; you can build the remaining workflows according to your use case.

        - Go to AI agent configuration and ensure you associate your AI agent workflows with the correct Action triggers. Save, preview, and republish the AI Agent.

        - Go to WebexCC Flows and import the voice flow 'CumulusAir_Voice_AIAgent.json'. Select the TTS connector and your AI agent from the Virtual Agent V2 node. Publish it and associate it with your voice inbound channel/entry point to test the flow."


**DEMO-3 CumulusAir PostFly - AI Powered Email Channel**

        - Import 'CumulusAir-EmailwithAIAgent.workflow' within your Connect service.

        - Go to settings and customer variables, then change the 'bizemailid' to your business email ID (email asset) and the queueId (refer to Control Hub > Email Queue).

        - Select the 'CumulusAir_AIAgent' from the AI Agent node, configure the remaining nodes as required, and publish the flow to test it.


_All the best !!_
