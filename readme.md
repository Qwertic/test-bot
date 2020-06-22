# A simple bot to integrate in slack
*Based on [Flottbot](https://target.github.io/flottbot-docs/about/) project*
**Install Your Bot Integration**

Got access to a Slack workspace? Great. Let's add your integration:

1. Go to the your Workspace's App Directory, search for 'Bots' and click the option Bots Connect a bot to the Slack Real Time Messaging API.

2. Click on the green Add Configuration button on the left.

3. Enter your chosen username for your bot and click on the green Add bot integration.

4. You should now be able to access your bot's Integration Settings where you will find your bot's API Token, which will look like xoxb-xxxxxxxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxx.

Hooray! Now let's run your bot in your workspace.

Edit the name of your bot in /config/bot.yml to look like:
`name: my-super-bot`
Now, you'll need to export your Slack bot token as an environment variable wherever your bot runs:

`export SLACK_TOKEN=xoxb-xxxxxxxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxx`
**Run**
*Docker is needed on your local machine in order to run the program*

`docker run --rm --name [container_name] --env SLACK_TOKEN=$SLACK_TOKEN -v "$PWD"/config:/config target/flottbot:latest /flottbot`

Your bot should now be online in the Slack Workspace you added the integration to.

On the bottom left side panel, you should see the Apps heading. Click on the circular + button.

1. In the Browse Apps search bar, enter your bot's username. Your bot should appear as a result.
2. Click on it. You should now see your bot online under the Apps heading of the side panel.

3. Message it hello and it should respond what's up?
