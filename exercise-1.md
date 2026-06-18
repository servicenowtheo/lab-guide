## Exercise 1: Voice Assistant Configuration and Testing

> **Use the guided setup experience within Assistant Designer to explore your Voice Assistant**

1. In the navigation menu, go to: **All > Conversational Interfaces > Assistant Designer**
2. From the *Assistants* pane, select **Now Assist Voice Deployment.**
3. From the *AI Agents* pane, you will see a list of agents already assigned to the Assistant. There should be one agent **Create incident with voice AI agent** active already. We will activate an additional agent.

![AI Agents pane showing assigned agents for Now Assist Voice Deployment](.gitbook/assets/LAB8114-K26/ex1-step3-ai-agents-pane.png)

4. Select the **Manage incident with voice AI agent** from the list.
5. Navigate to the **Select channels and status** section and toggle the agent active and click **Done.**
6. Now navigate back to the Assistant Designer and you should see the agent is active.
7. Navigate to the **Settings** tab. In the *Basic Details* pane, feel free to edit with sample details:
   - **Name:** IT Service Desk Assistant
   - **Description:** AI Voice Assistant that will handle Tier 0 calls across the technology organization - creating incidents, processing requests, providing INC/CHG status, troubleshooting Apps, and more.
   - **Tags:** Choose the tag icon on the right. Then type `Technology`, followed by Enter, to apply the new tag
   - Select **Save and Continue**

8. In the *Voice Personality* pane, fill in the following details:
   - **Language:** English
   - **Welcome Message:** Hello, and thank you for calling Otto Enterprises. How may I assist you today?
   - **Persona:** Explore a few of the voice personas, using the play button to sample the voices.
   - Select the **Help Desk Man** persona and then tap **Save and Continue**

9. In the *Communication Channels* pane, we will be using a dummy Twilio setup for testing purposes:
   - **Provider:** Twilio
   - **Provider application:** AI Voice Agent Provider Application
   - **Phone number to live agent:** *any number can work here*
   - **Authentication token:** *any number sequence can work here*
   - Select **Save and Continue**

   > In your instance, you will either configure for a CCaaS Integration (Telephony Provider) or a Mobile App integration.

10. In the *Authentication* pane, review the following:
    - **Caller Identification:** Primary - Phone number
    - **Authentication:** Primary - SoftPIN

    > For today's lab session, we will not be changing the authentication methods, but you can explore the preconfigured settings.

11. In the *Safeguards* pane:
    - Select **Connect to a live agent**
    - Examine the values listed for the Max Call Duration and Inactivity Timeout call constraints
    - Select **Save and Continue**

    > Safeguards are a great way to ensure the Voice Agent delivers a premier caller experience. This includes the voice agent knowing when it's time to pass caller to a human agent or open a record for the issue.

12. Under the *Review* pane:
    - Review the selections that you made match the intended configuration in the exercise above.
    - Select **Save and Activate**

### Testing the Voice Assistant

We will use the Voice Agents Test Experience, located within the Assistant Designer, to test the AI Voice Agents you have built.

1. Navigate to Assistant Designer and locate your Voice Assistant.
2. Select **Test** and the Test Experience UI will launch in a separate window.
3. Toggle the dropdown in the upper left corner to **Chat** (instead of Voice).
4. Click the **Start Call** button. You will need to accept the microphone permissions in your browser to allow audio to process. You may need to click **Restart** if you see the timer count up but not the initial greeting message.

> **NOTE:** For those with noise cancelling headphones, you can also opt to conduct your own voice based test (now or once you have completed all other exercises), just please be mindful of your volume.

**Test conversation flow:**

1. The Voice Agent test will begin with: *"Hi, I am your voice assistant. How may I help you today?"*
2. Proceed in the chat based conversation with a goal of testing both the OOB 'Incident Creation', as well as the Manage ticket agent.
3. Key Phrases during the conversation are likely to include:
   - "Can you help me create a ticket?"
   - "Do I have any open tickets?"
   - "What can you help me with?"
4. Hit **End Call** to conclude a test run.

> AI Voice Agents use an LLM to reason through each interaction, which means the path to resolution may vary from call to call — that's by design. Rather than following a fixed script, the agent adapts based on what the caller says. Use the **Restart** button to re-initiate the Voice Agent test if needed.

---

