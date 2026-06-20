# 🎬 Mehram - Browser Video Generator

Mehram is a powerful, easy-to-use browser-based video generation library. Create dynamic, animated videos directly in your browser without any server-side processing.

## ✨ Features

- 🎨 **Canvas-based rendering** - Draw high-quality frames directly on HTML5 Canvas
- 🎬 **Animation support** - Keyframe-based animations with easing functions
- 📝 **Text rendering** - Add stylized text to your videos
- 🎭 **Multiple shapes** - Rectangles, circles, triangles with customizable colors
- ⚡ **Real-time preview** - See changes instantly with the preview feature
- 📥 **Video export** - Export videos in multiple formats
- 🔧 **TypeScript** - Fully typed for better developer experience
- 🚀 **No dependencies** - Uses native browser APIs

## 🚀 Quick Start

### Browser Usage

1. Open `index.html` in your browser
2. Use the interactive controls to:
   - Customize video content (title, text, colors)
   - Adjust shapes and animations
   - Set video duration
3. Click "Preview" to see a quick animation
4. Click "Generate Video" to create your video
5. Download the generated video

### Programmatic Usage

```typescript
import { VideoGenerator, CanvasRenderer } from '@rameshprasad2251/mehram';

// Create a video generator
const video = new VideoGenerator({
  width: 1280,
  height: 720,
  fps: 30,
  duration: 10,
  format: 'mp4'
});

// Define a scene
const scene = {
  id: 'scene-1',
  duration: 5,
  elements: [
    {
      type: 'text',
      id: 'title',
      text: 'Hello Mehram!',
      fontSize: 48,
      fontFamily: 'Arial',
      color: '#667eea',
      x: 100,
      y: 100,
      width: 500,
      height: 100,
      animations: [
        {
          name: 'fadeIn',
          startTime: 0,
          duration: 2,
          keyframes: [
            { time: 0, properties: { opacity: 0 } },
            { time: 2, properties: { opacity: 1 } }
          ]
        }
      ]
    }
  ]
};

// Add scene and render
video.addScene(scene);

// Render with progress callback
const videoBlob = await video.render({
  onProgress: (progress) => console.log(`Rendering: ${progress * 100}%`)
});

// Use the blob (download, upload, etc.)
```

## 📖 API Documentation

### VideoGenerator

Main class for creating and managing videos.

```typescript
new VideoGenerator(config: VideoConfig)
```

**Methods:**
- `addScene(scene: Scene): this` - Add a scene
- `addScenes(scenes: Scene[]): this` - Add multiple scenes
- `clearScenes(): this` - Clear all scenes
- `getScenes(): Scene[]` - Get current scenes
- `render(options?: RenderOptions): Promise<Blob>` - Render video to blob
- `preview(canvas: HTMLCanvasElement): Promise<void>` - Preview on canvas

### Scene

A scene represents a time slice of the video with elements.

```typescript
interface Scene {
  id: string;
  duration: number;      // in seconds
  elements: Element[];
  transitions?: Transition[];
}
```

## 🔄 Browser Support

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+

---

**Happy video generating! 🎬✨**
