# SHNU---CS-330--OpenGL_Render
### Displaying some 3D rendering completed in my Comp Graph and Visualization class at SNHU
My time throughout this semester was my first time working with OpenGL, and I had very little experience with 3D modeling in general. I learned a lot about creating 3D computated graphic visualizations, and look forward to applying the skills that I have gained in future projects. 
The main goal of the project was to take a photo of various objects composed of relatively simple shapes, and to create a 3D render of the photo. To accomplish this task, I created a list of what simple shapes I would need to create to construct the more complex shapes to represent the objects in the photo.
The reference photo consisted of a pencil, a coffee mug, a teapot, and a spiral notebook all resting on a kitchen countertop. I came to the conclusion that I would render the objects using the following shapes:

* Pencil - Small pyramid for pencil tip, elongated cylinder for base of pencil, and small sphere for eraser
* Spiral notebook - Series of small toruses for spirals, 2 planes to make up the top and bottom covers, and a compressed cube that had the same dimensions (other than thickness) as the plane covers to represent paper
* Mug - Cylinder for the base of the mug, and a cut-off torus for the mug handle
* Teapot - Top half of sphere for the base of the teapot, top half of a torus for teapot handle, small sphere on top of the teapot base to represent lid handle, and a small tilted cylinder for a teapot spout.
* Countertop - A large textured plane
  
With this plan in mind, I knew that the shapes that I would have to define vertex, texture, and normal coordinates for would be a cylinder, torus, cube, sphere, pyramid, and plane. Instead of re-defining these coordinates every time I needed to use one of the shapes, I adjusted the model matrix each time one of the shapes were called, scaling, translating, and rotating the shape to whatever was required. I also changed the texture for each instance of the shape to whatever was needed. I also created a separate shader program to generate light, and rendered a small light cube above all of the objects to simulate the lighting conditions of the room the photo was taken in. When defining shape vertices, the most complicated one was the sphere, which required a fair amount of research to find how to calculate. The main source that I used to help understand sphere rendering is the following:
http://www.songho.ca/opengl/gl_sphere.html

Due to the extensive requirements for sphere generation, I kept the sphere in a separate CPP and header file and included it in the main rendering file for organizational purposes. 

Additionally, I added user controls to the program, so that anyone who is running the program can explore the scene using their keyboard and mouse. If the user presses the "P" key, the scene switches between a perspective and orthographic projection. 

After completing this project, I now have a much more clear understanding of computer graphics, and feel confident in my ability to create simple 3D renders for any future projects or needs, and look forward to building my skills to create more complex, quality renders. This project was also a nice experience for me to get more comfortable with C++ and implementing C++ libraries, as well as studying library documentation to build more efficient code. 

