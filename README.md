# Reveal.js + Astro Template

A minimalist template for creating beautiful presentations on the web using [Reveal.js](https://revealjs.com/) and [Astro](https://astro.build/).

## 🚀 Getting Started

### Prerequisites

- Node.js (version 18 or higher)
- pnpm (recommended) or npm

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd slides-template

# Install dependencies
pnpm install

# Start development server
pnpm dev
```

### Build for Production

```bash
pnpm build
```

## 📁 Project Structure

```
src/
├── components/
│   ├── Slide.astro          # Main slide component with all Reveal.js props
│   └── CodeBlock.astro      # Code highlighting component
├── layouts/
│   └── Layout.astro         # Base layout with Reveal.js setup
├── pages/
│   └── index.astro          # Main presentation page
└── slides/
    ├── Title.astro          # Title slide
    ├── WhyAstro.astro      # Example content slides
    ├── Test.astro          # Demo of background features
    ├── TestCode.astro      # Code highlighting examples
    └── Fit.astro           # Text fitting example
```

## 🎨 Available Slides

### Title.astro

The opening slide of your presentation. Contains the title, author, and event information.

### WhyAstro.astro

Example slides demonstrating:

- Basic content slides
- Fragment animations
- List presentations

### Test.astro

Comprehensive demo of background features including:

- Solid color backgrounds
- Video backgrounds with auto-loop and mute
- Linear, radial, and conic gradients
- Image backgrounds with sizing and repeat options

### TestCode.astro

Code presentation examples featuring:

- Syntax highlighting
- Line number highlighting
- Code animations
- Multiple language support

### Fit.astro

Text fitting demonstration using the `r-fit-text` class to automatically size text to fit the slide.

## 🎛️ Slide Component Props

The `<Slide>` component supports all Reveal.js slide attributes. Here are the main categories:

### Animation

- `animate?: boolean` - Enable/disable auto-animate (default: true)

### Backgrounds

All background props are documented in [Reveal.js Backgrounds](https://revealjs.com/backgrounds/)

**Colors:**

- `data-background-color?: string` - Solid background color

**Videos:**

- `data-background-video?: string` - Video source URL
- `data-background-video-loop?: boolean` - Loop video
- `data-background-video-muted?: boolean` - Mute video audio

**Gradients:**

- `data-background-gradient?: string` - CSS gradient (linear, radial, conic)

**Images:**

- `data-background-image?: string` - Image URL
- `data-background-position?: string` - Image position (default: center)
- `data-background-repeat?: string` - Image repeat behavior
- `data-background-size?: string` - Image sizing (cover, contain, etc.)
- `data-background-opacity?: number` - Background opacity (0-1)

### Transitions

Transition props are documented in [Reveal.js Transitions](https://revealjs.com/transitions/)

- `data-transition?: string` - Transition style (none, fade, slide, convex, concave, zoom)
- `data-transition-speed?: string` - Transition speed (default, fast, slow)

## 📝 Usage Examples

### Basic Slide

```astro
<Slide>
  <h2>Hello World</h2>
  <p>This is a basic slide</p>
</Slide>
```

### Gradient Background

```astro
<Slide data-background-gradient="linear-gradient(to bottom, #283b95, #17b2c3)">
  <h2>Beautiful Gradient</h2>
</Slide>
```

### Video Background

```astro
<Slide
  data-background-video="./video.mp4"
  data-background-video-loop={true}
  data-background-video-muted={true}
>
  <h2>Video Background</h2>
</Slide>
```

### Custom Transition

```astro
<Slide
  data-transition="zoom"
  data-transition-speed="fast"
>
  <h2>Zoom In Fast!</h2>
</Slide>
```

### Code Highlighting

```astro
<pre>
  <code class="language-js" data-trim data-line-numbers="1-3">
    {`function hello() {
      console.log("Hello, World!");
      return true;
    }`}
  </code>
</pre>
```

## 🔧 Customization

### Adding New Slides

1. Create a new `.astro` file in `src/slides/`
2. Import and use the `<Slide>` component
3. Import your slide in `src/pages/index.astro`
4. Add it to the presentation

### Styling

- Global styles are in `src/layouts/Layout.astro`
- Reveal.js themes can be changed in the Layout component
- Custom CSS can be added using Astro's styling features

### Configuration

Reveal.js configuration is in `src/layouts/Layout.astro`. You can modify:

- Transitions
- Controls
- Progress bar
- History
- Plugins

## 📚 Documentation

- **Reveal.js Official Docs**: [https://revealjs.com/](https://revealjs.com/)
- **Backgrounds**: [https://revealjs.com/backgrounds/](https://revealjs.com/backgrounds/)
- **Transitions**: [https://revealjs.com/transitions/](https://revealjs.com/transitions/)
- **Auto-Animate**: [https://revealjs.com/auto-animate/](https://revealjs.com/auto-animate/)
- **Code Highlighting**: [https://revealjs.com/code/](https://revealjs.com/code/)
- **Astro Documentation**: [https://docs.astro.build/](https://docs.astro.build/)

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
