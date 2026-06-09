# 🗺️ Advanced Dungeon Map Designer

A powerful web-based tool for designing and editing dungeon maps with a visual grid editor, array manipulation, and AI-powered assistance.

## Features

### Visual Editor
- **Interactive Grid**: Click and drag to paint tiles directly on the map
- **Tile Types**: Floor, Wall, Door In (entry), Door Out (exit)
- **Grid Toggle**: Show/hide grid overlay for precise alignment
- **Real-time Rendering**: See changes instantly as you paint

### Array Editor
- **Direct Editing**: Edit the 2D array representation directly
- **Update Visual Button**: Instantly render changes from the array editor
- **Paste Support**: Paste existing dungeon arrays and visualize them
- **Copy/Export**: Get your map as a properly formatted JavaScript array

### Procedural Generation
- **Room Builder**: Generate multi-room dungeons automatically
- **Templates**: Load pre-built templates (Maze, Cathedral, Simple)
- **Custom Dimensions**: Set width and height (5-50)
- **Door Placement**: Position entry and exit doors where you want them

### AI Assistant (Groq Integration)
- **Natural Language Modifications**: Describe changes in plain English
- **Smart Map Generation**: AI understands dungeon design concepts
- **API Integration**: Uses Groq's Qwen model for fast, reliable responses
- **Example Commands**:
  - "Add obstacles in the middle"
  - "Make a corridor on the left"
  - "Add a chamber in the center"
  - "Make it more maze-like"

### Door Coordinate Detection
- **Automatic Detection**: Find the exact coordinates where characters enter/exit
- **RenPy Format**: Output formatted for direct use in visual novels
- **Copy to Clipboard**: Easy export of door coordinates

### Quality of Life
- **Dark Mode**: Easy on the eyes during long design sessions
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Instant Feedback**: Real-time logging of all actions
- **Persistent Settings**: Dark mode preference is saved locally

## Getting Started

### Basic Usage
1. Open `index.html` in your web browser
2. Configure map dimensions (Width/Height)
3. Select a tile type (Floor, Wall, Door In, Door Out)
4. Click and drag on the visual grid to paint
5. View the array editor for the 2D array representation

### Using the Update Visual Button
1. Edit or paste an array in the **Array Editor** textarea
2. Click the **"Update Visual"** button
3. The map will instantly render on the visual grid
4. This is useful for importing existing maps or making bulk changes

### Using Templates
1. Select your preferred map size using the Configuration panel
2. Click one of the template buttons:
   - **🌀 Maze**: Generates a maze-like structure
   - **🏛️ Cathedral**: Creates a large central chamber with side rooms
   - **📦 Simple**: Creates 2-3 connected rectangular rooms

### Using Room Builder
1. Select the number of rooms (2, 3, or 4)
2. Choose entry position (Door In location)
3. Choose exit position (Door Out location)
4. Click **"Generate Connected Rooms"**
5. Rooms are automatically connected with doorways

### Using AI Assistant
1. Get a free Groq API key at [console.groq.com/keys](https://console.groq.com/keys)
2. Paste your API key in the **Groq API Key** field
3. Describe your desired modification in plain English
4. Click **"Send"** or press Enter
5. The AI will modify your map and display the result

**Tips for AI Requests**:
- ✅ Simple, single requests work best
- ⚠️ Complex multi-room requests may fail - break them into 2-3 separate calls or build manually
- 💡 Be specific and concise

### Getting Door Coordinates
1. Design your map with entry and exit doors
2. Click **"Detect Doors"** button
3. Coordinates appear in the textarea below
4. Click **"Copy Code"** to copy to clipboard
5. Use in your game engine (e.g., RenPy visual novels)

## Tile Types

| Tile | Value | Color | Description |
|------|-------|-------|-------------|
| Floor | 0 | Gray | Walkable area |
| Wall | 1 | Black | Solid obstacle |
| Door Out | 2 | Green | Exit/Door leading out |
| Door In | 3 | Blue | Entry/Door leading in |

## Array Format

Maps are stored as 2D JavaScript arrays:

```javascript
[
  [1,1,1,1,1],
  [1,0,0,0,1],
  [1,0,0,0,1],
  [1,1,3,1,1],
  [1,1,2,1,1]
]
```

You can:
- Edit arrays directly in the **Array Editor**
- Click **"Update Visual"** to render changes
- Export arrays from the editor for use in other projects

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- No installation or dependencies required
- Optional: Groq API key for AI features

## Getting a Groq API Key

1. Visit [console.groq.com](https://console.groq.com)
2. Sign up for a free account
3. Navigate to API Keys
4. Create a new API key
5. Copy and paste it into the Dungeon Map Designer

Free tier includes generous API limits for personal use!

## Keyboard Shortcuts

- **Enter** (in chat input): Send AI request
- **Click and Drag**: Paint on the grid
- **Grid Toggle**: Show/hide grid lines for cleaner view

## Use Cases

- **Game Development**: Design levels for RPGs and dungeon crawlers
- **Tabletop Gaming**: Create battle maps for D&D, Pathfinder, etc.
- **Visual Novel Development**: Build locations with RenPy integration
- **Educational Projects**: Learn about procedural generation
- **Story Writing**: Visualize settings for written narratives

## Tips for Best Results

1. **Start Simple**: Begin with basic room layouts, add complexity gradually
2. **Use Templates**: Templates are great starting points
3. **Test Your Map**: Ensure doors lead to valid floor tiles
4. **Room Builder First**: Use procedural generation for basic structure, then refine manually
5. **AI for Details**: Use AI for adding obstacles and features, not entire rooms
6. **Coordinate Validation**: Always run door detection before exporting

## Browser Compatibility

- ✅ Chrome/Chromium 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

## License

The Unlicense - Free to use for any purpose

## Support

For issues or suggestions:
1. Check the tips panel in the application
2. Verify your Groq API key format (starts with `gsk_`)
3. Try simpler AI requests
4. Use procedural generation or manual painting as fallbacks

---

**Happy Map Designing! 🗺️✨**
