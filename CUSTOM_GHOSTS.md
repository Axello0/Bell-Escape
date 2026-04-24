# Custom Ghost Images Guide

You can now customize the ghosts in Pac-Man by replacing them with your own images!

## How to Add Custom Ghost Images

### Step 1: Add Your Images
Place your ghost image files in the same folder as `pacman.js` and `index.html`. 

**Recommended:**
- Image format: PNG or JPEG
- Image size: Square (e.g., 50x50px, 100x100px)
- The game will automatically scale them to fit the game board

### Step 2: Edit the Ghost Specs
Open `pacman.js` and find this section (around line 840):

```javascript
ghostSpecs   = [
    { color: "#00D9FF", name: "Cyan", image: null },
    { color: "#FF4444", name: "Red", image: null },
    { color: "#FF69B4", name: "Pink", image: null },
    { color: "#FFA500", name: "Orange", image: null }
],
```

Replace `null` with the path to your image file:

```javascript
ghostSpecs   = [
    { color: "#00D9FF", name: "Cyan", image: "ghost1.png" },
    { color: "#FF4444", name: "Red", image: "ghost2.png" },
    { color: "#FF69B4", name: "Pink", image: "ghost3.png" },
    { color: "#FFA500", name: "Orange", image: "ghost4.png" }
],
```

### Step 3: Test
Refresh the page in your browser. The custom images should appear!

## Tips

- **If an image fails to load**, the game will automatically fall back to the original colored ghost shapes
- **Image transparency**: Use PNG with transparency for best results
- **Relative paths**: Use paths relative to `index.html` (e.g., `"ghost1.png"` or `"images/ghost1.png"`)
- **Keep it small**: Smaller images load faster

## Example

If you have images named `blinky.png`, `pinky.png`, `inky.png`, and `clyde.png`:

```javascript
ghostSpecs   = [
    { color: "#00D9FF", name: "Cyan", image: "blinky.png" },
    { color: "#FF4444", name: "Red", image: "pinky.png" },
    { color: "#FF69B4", name: "Pink", image: "inky.png" },
    { color: "#FFA500", name: "Orange", image: "clyde.png" }
],
```

Save and refresh!
