# 🎬 Mehram - Browser-Based Video Generator

A powerful, lightweight browser-based video generation tool that runs entirely in your browser. No server required, no complex setup. Just pure client-side video creation magic!

## ✨ Features

- **Browser-Based**: Generate videos directly in your browser with zero server dependencies
- **Real-Time Preview**: See changes instantly with live preview functionality
- **Customizable**: Full control over dimensions, duration, colors, fonts, and animations
- **Multiple Animations**: Choose from Fade In, Slide In, Zoom In, Rotate, or None
- **Easy Download**: Generate and download videos in WebM format
- **Responsive Design**: Works seamlessly on desktop and tablet devices
- **No Installation**: Just open the HTML file and start creating!

## 🚀 Quick Start

### Method 1: Direct File Access
1. Clone the repository:
   ```bash
   git clone https://github.com/rameshprasad2251/Mehram.git
   cd Mehram
   ```

2. Open `index.html` in your browser:
   - Double-click the file, or
   - Right-click → Open with Browser, or
   - Use a local server: `python -m http.server 8000`

### Method 2: GitHub Pages
1. Enable GitHub Pages in repository settings
2. Set source to `main` branch
3. Access your site at: `https://rameshprasad2251.github.io/Mehram/`

## 📖 Usage Guide

### Configuration Panel
- **Video Title**: Set the text that appears in your video
- **Width/Height**: Video dimensions in pixels (default: 1280x720)
- **Duration**: Video length in seconds (1-60 seconds)
- **FPS**: Frames per second (15-60 FPS)
- **Text Color**: Choose any color for your text
- **Background Color**: Set the video background
- **Font Size**: Adjust text size (12-120px)
- **Animation Type**: Select animation style for text

### Buttons
- **👁️ Preview**: See real-time preview without generating a full video
- **🎥 Generate Video**: Create a complete video file
- **⬇️ Download Video**: Download your generated video

## 🎨 Animation Types

- **None**: Static text display
- **Fade In**: Text gradually appears
- **Slide In**: Text slides in from the left
- **Zoom In**: Text zooms from small to full size
- **Rotate**: Text spins into view

## 💾 Technical Details

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Video Encoding**: MediaRecorder API + WebM codec
- **Canvas**: HTML5 Canvas 2D for rendering
- **No Dependencies**: Pure vanilla JavaScript

### Browser Compatibility
- ✅ Chrome 49+
- ✅ Firefox 25+
- ✅ Safari 14.1+
- ✅ Edge 79+

### Performance Notes
- Video generation happens on your device
- Larger resolutions and longer durations take more processing time
- For 4K or 60+ second videos, allow extra processing time
- Check browser console for any errors

## 🔧 Customization

### Modify Colors
Edit the color values in the Configuration panel or directly in the HTML:
```html
<input type="color" id="textColor" value="#667eea">
<input type="color" id="backgroundColor" value="#ffffff">
```

### Change Default Values
Modify the default values in input fields:
```html
<input type="number" id="videoWidth" value="1280" min="320">
<input type="number" id="videoHeight" value="720" min="240">
```

### Add Custom Animations
Edit the `SimpleMehramGenerator` class in the script section to add new animation types.

## 📁 Repository Structure

```
Mehram/
├── index.html          # Main application file
├── README.md           # This file
├── LICENSE             # MIT License
└── docs/
    ├── GUIDE.md        # Detailed usage guide
    ├── API.md          # API documentation
    └── examples/       # Example configurations
```

## 🐛 Troubleshooting

### Video won't generate
- Check browser console (F12) for errors
- Ensure video duration is between 1-60 seconds
- Try reducing resolution if experiencing lag

### Download button disabled
- Generate a video first using "🎥 Generate Video" button
- Check that your browser allows downloads

### Slow performance
- Reduce video resolution
- Lower FPS to 24 or 30
- Reduce duration

### No audio in video
- This tool generates video-only files. Add audio in post-processing using:
  - FFmpeg
  - Video editing software (DaVinci Resolve, Adobe Premiere, etc.)

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋 Support

- **Issues**: Report bugs on the [GitHub Issues](https://github.com/rameshprasad2251/Mehram/issues) page
- **Discussions**: Join the [GitHub Discussions](https://github.com/rameshprasad2251/Mehram/discussions) for questions and ideas
- **Documentation**: Check the [docs](docs/) folder for detailed guides

## 📚 Resources

- [HTML5 Canvas Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [MediaRecorder API](https://developer.mozilla.org/en-US/docs/Web/API/MediaRecorder)
- [WebM Format](https://www.webmproject.org/)

## 🎯 Roadmap

- [ ] Audio support
- [ ] Multiple text elements
- [ ] Image/video background support
- [ ] Preset templates
- [ ] MP4 export format
- [ ] Cloud sharing capabilities
- [ ] Mobile app version

## 👨‍💻 Author

**Ramesh Prasad**
- GitHub: [@rameshprasad2251](https://github.com/rameshprasad2251)

---

Made with ❤️ for video creators everywhere. Happy creating! 🎬
