# minilibX

### MiniLibX is a simple (X-Window (X11R6) programming API in C) and lightweight graphics library often used in educational settings in 42 School network. It's designed to help students learn the basics of graphical programming in a straightforward, hands-on manner. Here's an overview of its features and usage:

## Contents:
- source code in C to create the mlx library
- man pages (in man/ directory)
- a public include file mlx.h
- a tiny configure script to generate an appropriate Makefile.gen

## Requirements for MacOS:
- **downloading Xquartz**, you can download Xquartz here in the link below ⬇️:
- [Xquartz](https://www.xquartz.org/)
```
➜  ~ Brew install Xquartz
➜  ~ reboot
➜  ~ xeyes # run an hello world X11 app
```

## Key Features of MiniLibX 🔑:

- **Window Management:** MiniLibX allows you to create and manage windows. This is fundamental for any graphical application.
- **Image Rendering:** It provides functionalities to create, manipulate, and display images. This is essential for drawing graphics.
- **Event Handling:** MiniLibX can handle basic events such as keyboard and mouse inputs, allowing for interactive applications.
- **Pixel Manipulation:** It offers the ability to manipulate individual pixels, enabling custom drawing and effects.
- **Cross-Platform:** While primarily used on Unix-based systems, MiniLibX can also work on macOS, offering some level of cross-platform capability.

## Using MiniLibX ⚙️:
- **Setting Up:** The first step is to set up MiniLibX in your development environment. This typically involves installing the library and linking it with your C projects.
- **Creating a Window**: You start by creating a window using MiniLibX functions. This window is where all your graphics will be displayed.
- **Drawing:** You can draw shapes, images, and manipulate pixels within the window. MiniLibX provides functions to put pixels at specific coordinates, which is the basis for more complex drawings.
- **Handling Events:** Implementing event listeners allows your application to respond to user inputs like keyboard presses or mouse movements.
- **Animation and Updating the Screen**: By continually updating the screen and changing the graphics, you can create animations.

## Limitations 🚩:
- **Simplicity:** MiniLibX is quite basic compared to more advanced graphics libraries like OpenGL or DirectX. It's more suited for educational purposes rather than developing complex, high-performance graphical applications.
- **Documentation:** The documentation for MiniLibX can be sparse and sometimes not as comprehensive as for other libraries. Much of the learning may come from community forums, example projects, and trial and error.
- **Performance:** Being a simple library, it may not be the most efficient choice for graphics-intensive applications.

## Educational Value 📝:
MiniLibX is particularly valuable for educational purposes. It forces you to understand low-level graphics programming concepts without the overhead of more complex libraries. This can be a great foundation before moving on to more advanced graphics programming.

# minilibx functions📎:

## 1)Window Management:
- **mlx_init():** Initializes the connection to the display (often considered as starting point of the MiniLibX application).
- **mlx_new_window():** Creates a new window. You specify the size and title of the window.

## 2)Image Manipulation:
- **mlx_new_image():** Creates a new image in memory. Useful for off-screen drawings or preparing graphics before displaying them.
- **mlx_get_data_addr():** Retrieves the address of the pixel data of an image. This is essential for direct pixel manipulation.
- **mlx_put_image_to_window():** Places an image onto a window. This is how you display your prepared image.

## 3)Drawing:
- **mlx_pixel_put():** Puts a single pixel on the window. Basic but crucial for drawing anything.
- **mlx_string_put():** Displays a string on the window. Useful for adding text labels or UI elements.

## 4)Event and Hook Management:
- **mlx_key_hook():** Sets up a function to be called when a keyboard key is pressed while the specified window is focused.
- **mlx_mouse_hook():** Similar to mlx_key_hook, but for mouse clicks.
- **mlx_expose_hook():** Sets a function to be called when a window is exposed (becomes visible). Useful for redrawing the content.
- **mlx_loop():** Starts the MiniLibX loop to keep the application running. This is where it listens for events and continuously renders.

## 5)Utility and Miscellaneous:
- **mlx_clear_window():** Clears a window. Often used before redrawing the entire content.
- **mlx_destroy_window():** Closes a window and frees its resources.
- **mlx_destroy_image():** Frees the memory allocated for an image.
- **mlx_loop_hook():** Adds a function to the main loop, allowing you to perform actions like animations.

## Usage Notes🚨:
- **Direct Pixel Manipulation:** MiniLibX allows you to directly manipulate pixels of an image. After creating an image with mlx_new_image and getting its data address with `mlx_get_data_addr()`, you can alter pixels to render custom graphics.
- **Event Handling:** The library's approach to event handling with `mlx_key_hook()`, `mlx_mouse_hook()`, and others, is straightforward but requires you to structure your application to continuously listen and respond to these events.
- **Main Loop:** The `mlx_loop` function is essential as it keeps your application running and responsive. It's where all the event handling and continuous rendering happens.














