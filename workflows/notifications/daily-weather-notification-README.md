# Daily Weather Notification

Get daily weather updates sent to your Slack channel every morning.

## Description

This workflow fetches weather data from OpenWeatherMap API and sends a formatted notification to Slack every morning at 8:00 AM.

## Prerequisites

- n8n instance (self-hosted or cloud)
- OpenWeatherMap API key (free tier available at [openweathermap.org](https://openweathermap.org/api))
- Slack workspace with a configured incoming webhook or bot

## Setup Instructions

1. **Import the Workflow**
   - Download `daily-weather-notification.json`
   - In n8n, go to Workflows → Import from File
   - Select the downloaded file

2. **Configure OpenWeatherMap API**
   - Get your API key from [OpenWeatherMap](https://openweathermap.org/api)
   - In the "Get Weather" node, replace `YOUR_API_KEY` with your actual API key
   - Replace `Your City Name` with your desired city

3. **Configure Slack Credentials**
   - Click on the "Send Notification" node
   - Create new Slack credentials or select existing ones
   - Test the connection

4. **Customize the Schedule**
   - The workflow runs daily at 8:00 AM (0 8 * * *)
   - Click "Schedule Trigger" to change the time
   - Use [Crontab.guru](https://crontab.guru/) to create custom schedules

5. **Activate the Workflow**
   - Click the "Active" toggle in the top right
   - The workflow will now run automatically

## How It Works

1. **Schedule Trigger**: Runs every day at 8:00 AM
2. **Get Weather**: Calls OpenWeatherMap API to fetch current weather
3. **Send Notification**: Formats and sends the weather data to Slack

## Customization

### Change Temperature Units
In the "Get Weather" node, modify the `units` parameter:
- `metric` for Celsius
- `imperial` for Fahrenheit
- `standard` for Kelvin

### Modify the Message
Edit the text in the "Send Notification" node to customize the message format.

### Send to Different Channels
Configure the Slack node to send to specific channels or users.

## Use Cases

- Start your day informed about the weather
- Plan outdoor activities
- Know when to carry an umbrella
- Coordinate team activities based on weather

## Notes

- The free tier of OpenWeatherMap allows 1,000 API calls per day
- Make sure your n8n instance is running when the scheduled time arrives
- Test the workflow manually before activating

## Troubleshooting

**API Error**: Verify your OpenWeatherMap API key is correct
**City Not Found**: Check the spelling of your city name
**Slack Not Receiving**: Verify Slack credentials and channel permissions
