# Copilot Studio

## Recommendations

### Handle User Inactivity

- Go to Topics Tab
- Click on Add a Topic > From Blank
- A default Trigger is show - **The agent chooses** > Change it to **User is inactive for awhile**
- If needed show user a message, that the session is being reset
- Then add a node from **Variable Management** - **Clear variable values**
- It will have variable set to **Global variables for the current session** > change it to **Conversation history for current session**
- Finally add a node from **Topic Management** - **End Conversation**
