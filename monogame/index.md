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

```C#
Texture2D image = Content.Load<Texture2D>("[FileNameWithoutExtension]");
Texture2D image = Content.Load<Texture2D>("Backgrounds/Logo"); // with folder name

```

In `UnloadContent()` (and elsewhere), you can run code like this:

```C#
Content.Unload(); // not necessary for very small games.  You could create multiple `ContentManager` objects, so you don't unload *all* content.
```

## 2D Tutorials

### Tutorial 1 - Intro

http://rbwhitaker.wikidot.com/monogame-introduction-to-2d-graphics

#### Coordinate System

- Origin (0,0) is top left - so y-axis go down, not up
- not all screen sizes are the same, so width and height aren't known at build time
- a *sprite* is a 2D image

### Tutorial 2 - SpriteBatches

http://rbwhitaker.wikidot.com/monogame-spritebatch-basics

- Use the MonoGame Pipeline application to get content into the project
- Use instance variables to store sprites:
    ```C#
    private Texture2D background;
    ```
- Load them up in `LoadContent()` (or wherever):
    ```C#
    background = Content.Load<Texture2D>("filename");
    ```
- `spriteBatch` instance variable is already declared:
    ```C#
    SpriteBatch spriteBatch;
    ```
- its already initialised in `LoadContent()`:
    ```C#
    protected override void LoadContent()
    {
        // Create a new SpriteBatch, which can be used to draw textures.
        spriteBatch = new SpriteBatch(GraphicsDevice);
    ```
- You can draw (in `Draw()`) like this:
    ```C#
    spriteBatch.Begin();
    spriteBatch.Draw(background, new Rectangle(0, 0, 800, 480), Color.White);
    spriteBatch.Draw(earth, new Vector2(400, 240), Color.White); // vector2 says where to draw it
    spriteBatch.End();
    ```
- Order of drawing is important - things get drawn on top of other things
