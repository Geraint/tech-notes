# MonoGame notes

## Getting Started

### Tutorial 3 - the Visual Studio template

- `GraphicsDeviceManager` - talks to the graphic device
- `SpriteBatch` - tool to draw sprites
- `Initialize()` method - one time setup before game loop
- `LoadContent()` method - note that you can load content anywhere
- `Update()` method (by default, called 30 times per sec)
- `Draw()` method (also called 30 times per sec by default)

### Tutorial 4 - Managing Content

#### Store it

- Content is normally art assets (fonts, images, 3d models, sound effects, music, video)
- `Content\Content.mgcb` - open with MonoGame Pipeline application
- `Edit > Add > Existing Item`
- `Edit > Add > New Folder`

#### Using Content

In `LoadContent()` (and elsewhere), you can run code like this:

```
Texture2D image = Content.Load<Texture2D>("[FileNameWithoutExtension]");
Texture2D image = Content.Load<Texture2D>("Backgrounds/Logo"); // with folder name

```

In `UnloadContent()` (and elsewhere), you can run code like this:

```
Content.Unload(); // not necessary for very small games.  You could create multiple `ContentManager` objects, so you don't unload *all* content.
```

## 2D Tutorials

### Tutorial 1 - Intro

http://rbwhitaker.wikidot.com/monogame-introduction-to-2d-graphics

#### Coordinate System

- Origin (0,0) is top left - so y-axis go down, not up
- not all screen sizes are the same, so width and height aren't known at build time
- a *sprite* is a 2D image
