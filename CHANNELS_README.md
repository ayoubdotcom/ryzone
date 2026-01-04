# Editing Channels

This file (`channels.json`) contains all the YouTube channels displayed in the Rakiz app.

## How to Edit

You can add, remove, or modify channels by editing this JSON file. After building the app (`npm run build`), you can edit `dist/channels.json` directly without rebuilding.

## Channel Structure

Each channel object must have these fields:

```json
{
    "id": "unique-number",
    "name": "Channel Name",
    "thumbnail": "https://yt3.googleusercontent.com/...",
    "category": "Tech|Business|AI|Education|Fitness|Travel|Entertainment",
    "level": "Beginner|Intermediate|Advanced",
    "description": "Channel description",
    "youtubeId": "UCxxxxxxxxx"
}
```

## Finding YouTube Channel IDs

1. Go to the channel's YouTube page
2. View page source (Ctrl+U or Cmd+U)
3. Search for "channelId"
4. Copy the ID that looks like `UCxxxxxxxxx`

## Example: Adding a Channel

```json
{
    "id": "8",
    "name": "Kurzgesagt",
    "thumbnail": "https://yt3.googleusercontent.com/ytc/...",
    "category": "Education",
    "level": "Beginner",
    "description": "Animation videos explaining things.",
    "youtubeId": "UCsXVk37bltHxD1rDPwtNM8Q"
}
```

## Important Notes

- Each channel must have a unique `id`
- The `youtubeId` is required for fetching videos
- Valid categories: Tech, Business, AI, Education, Fitness, Travel, Entertainment
- Valid levels: Beginner, Intermediate, Advanced
- Make sure the JSON is valid (use a JSON validator if needed)
