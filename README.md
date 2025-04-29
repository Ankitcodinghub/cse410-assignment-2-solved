# cse410-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CSE410 Assignment 2 Solved](https://www.ankitcodinghub.com/product/cse410-table-of-contents-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;114147&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE410 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Prerequisites 1

Implementation of a Fully Controllable Camera 2

Taking and Processing Input 3

Implementation of the draw() Method 6

Implementation of the capture() and the intersect() Methods 6

Illumination with the Phong Lighting Model 7

Recursive Reflection 8

Implementation of the intersect() Method Revisited 9

Memory Management 10

Bonus Tasks 10

General Suggestions 10

Resources/References 11

Sample I/O 11

Submission Guidelines 15

______________________________________________________________________________

In this assignment, you have to generate realistic images for a few geometric shapes using ray tracing with appropriate illumination technique. [Blue text indicates the changes.]

Prerequisites

1. Basic knowledge of OpenGL (What you have learnt in assignment 1 should be sufficient)

2. Fully controllable camera (same as in assignment 1)

3. Bitmap image generation using the bitmap image header file provided for assignment 2

4. Basic idea of illumination, Phong lighting model to be more specific

5. Intersection of line with different 3D objects (e.g. ray-plane intersection, ray-sphere intersection, ray-triangle intersection etc.)

6. Multi-level reflection using ray tracing

7. Refraction using ray tracing (optional)

Implementation of a Fully Controllable Camera

You need to move and rotate the camera freely. Check the details from Assignment 1 if required.

Key Function Key Function

Up arrow Move forward 1 Rotate/Look left

Down arrow Move backward 2 Rotate/Look right

Left arrow Move left 3 Look up

Right arrow Move right 4 Look down

PageUp Move up 5 Tilt Clockwise

PageDown Move DOwn 6 Tilt Counterclockwise

Taking and Processing Input

1. Call a function named loadData() from your main function. This function should read a text file named “scene.txt” containing details of different objects (shapes) and lights present in the environment. There can be three types of objects (shapes) in the file sphere, triangle and object (shape) having a general quadratic equation in 3D. There will be two types of light sources – point lights and spotlights. In case of point lights, their color and position will be specified. And in case of the spotlights, their direction and cutoff angle will be specified in addition to the position and color information. Check the given “scene.txt” file for further clarification.

2. Create a separate header file/src file and define the classes here. The name of the file should have your student no. as prefix (e.g. 1705123_classes.h). Include this file in the cpp file containing the main function. This file should be named similarly, having your student no. as prefix (e.g. 1705123_main.cpp).

3. Create a base class named Object in the header/src file mentioned in Step 2. You should define separate classes for each object (shape), and all of them should inherit the Object class. The Object class can initially have the following methods and attributes. You can add or refactor later as appropriate.

Object{

Vector3D reference_point // should have x, y, z double height, width, length double color[3]

double coEfficients[4] // ambient, diffuse,

specular, reflection coefficients int shine // exponent term of specular component object(){} virtual void draw(){} void setColor(){} void setShine(){} void setCoEfficients(){}

}

The derived classes can use the attributes of the Object class. Each of them, however, must override the draw method. For example, you can design a Sphere class as follows.

Sphere : Object{

Sphere(center, radius){ reference_point = center length = radius

} void draw(){

// write codes for drawing sphere

} …

}

Besides, there can be two other classes named PointLight and SpotLight. The

PointLight{ Vector3D light_pos; double color[3]; …

}

The SpotLight class, on the other hand, should contain direction and cutoff angle in addition. So it can have a PointLight member variable and these two other properties.

SpotLight{

PointLight point_light; Vector3D light_direction; double cutoff_angle; …

}

Alternatively, you can use the idea of inheritance and implement the classes differently.

// declaration vector &lt;Object&gt; objects; vector &lt;PointLight&gt; pointLights; vector &lt;SpotLight&gt; spotLights;

// populating in the loadData() function Object *temp temp = new Sphere(center, radius); // received as input // set color

// set coEfficients // set shine objects.push_back(temp)

// construct a point light object, say, pl pointLights.push_back(pl)

// construct a spot light object, say, sl spotLights.push_back(sl)

5. Besides the objects given in the input file, you need to draw a floor. So create a Floor class which inherits the Object class (just like the other shapes). You need to write its draw method so that a checkerboard of two predefined alternating colors is drawn. You can choose the colors, reflection coefficients, shine (i.e. exponent term) etc. as you like.

// declaration

Floor: Object{

Floor(floorWidth, tileWidth){ reference_point=(-floorWidth/2,-floorWidth/2,0); length=tileWidth

}

Void draw(){

// write codes for drawing a checkerboard-like

// floor with alternate colors on adjacent tiles

}

}

// populating in the loadData() function

temp = new Floor(1000, 20) // you can change these values // set color

// set coEfficients // set shine objects.push_back(temp)

Implementation of the draw() Method

This is trivial as for spheres and triangles. You can use OpenGL functions and your code of assignment 1 for this purpose. Think about how you can draw the floor like a checkerboard. This is quite simple as well. However, you do not have to draw the general quadric surfaces. You only need to show them in the bmp image file, generated by capturing the scene, as elaborated next.

Implementation of the capture() and the intersect() Methods

1. Create a method capture() in MAIN_FILE which will be called when you press 0.

2. Create a class named Ray in the HEADER_FILE.

Ray{

Vector3D start;

Vector3D dir; // normalize for easier calculations

//write appropriate constructor

}

capture(){ initialize bitmap image and set background color planeDistance = (windowHeight/2.0) /

tan(viewAngle/2.0)

topleft = eye + l*planeDistance – r*windowWidth/2 +

u*windowHeight/2

du = windowWidth/imageWidth dv = windowHeight/imageHeight

// Choose middle of the grid cell topleft = topleft + r*(0.5*du) – u*(0.5*dv)

int nearest; double t, tMin; for i=1:imageWidth for j=1:imageHeight calculate curPixel using topleft,r,u,i,j,du,dv cast ray from eye to (curPixel-eye) direction double *color = new double[3] for each object, o in objects t = o.intersect(ray, dummyColor, 0) update t so that it stores min +ve value save the nearest object, on

tmin = on-&gt;intersect(ray, color, 1) update image pixel (i,j)

save image // The 1st image you capture after running

the program should be named Output_11.bmp, the 2nd image you capture should be named Output_12.bmp and so on.

4. In the Object class, create a virtual method intersect() as follows.

virtual double intersect(Ray *r, double *color, int level){ return -1.0;

}

5. In each of the derived classes, override the intersect() method. This will vary for each different object (shape). More specifically, you have to implement ray-sphere, ray-triangle, ray-general quadric surfaces, ray-floor etc. intersections for the different objects. Some of these are discussed in the theory classes.

6. Once you have implemented the intersect() method of a class, say, sphere, it is encouraged to test if your program works correctly. If not, then you can manually do the computations for a custom ray passing through a particular pixel and debug your code to find what went wrong.

Illumination with the Phong Lighting Model

In the intersect() method, after computing intersecting t of ray r, add some lighting codes. This method receives an integer level, as its last parameter, which actually determines if the ray currently under consideration will be reflected again or not. But this can be used to decide if a pixel should be colored or not as well.

1. When level is 0, the purpose of the intersect() method is to determine the nearest object only. No color computation is required then. (You could do this with some

different method as well, but the computations would be fairly similar.)

2. When level &gt; 0, add lighting codes according to the Phong model i.e. compute ambient, diffuse and specular components for each of the light sources and combine them.

3. After computing t, you can refactor your intersect() method as follows.

double intersect(Ray *r, double *color, int level){

// code for finding intersecting tmin

if level is 0, return tmin intersectionPoint = r-&gt;start + r-&gt;dir*tmin intersectionPointColor = getColorAt(intersectionPoint) color = intersectionPointColor*coEfficient[AMB] calculate normal at intersectionPoint

for each point light pl in pointLights cast rayl from pl.light_pos to intersectionPoint // if intersectionPoint is in shadow, the diffuse // and specular components need not be calculated if rayl is not obscured by any object

Recursive Reflection

To handle reflection, you need to do the same calculations as camera rays (i.e. the ones cast from the eye). The recursion_level (given as input) controls how many times a ray will be reflected when incident upon objects (shapes). Say, if recursion_level is set to 2, a camera ray should be reflected by objects (shapes) and the primary resulting reflected rays should also be reflected by other objects (shapes), but reflection will no longer have to be considered afterwards for the secondary reflected rays. You can do the following for reflection in the intersect() method after color computation.

double intersect(Ray *r, double *color, int level){

// code for finding color components if level ≥ recursion_level, return tmin

construct reflected ray from intersection point // actually slightly forward from the point (by moving the

// start a little bit towards the reflection direction) // to avoid self intersection find tmin from the nearest intersecting object, using intersect() method, as done in the capture() method if found, call intersect(rreflected, colorreflected, level+1)

// colorreflected will be updated while in the subsequent call

// update color using the impact of reflection color += colorreflected * coEfficient[REC_REFFLECTION] }

Implementation of the intersect() Method Revisited

(shapes). More precisely, ray-object (shape) intersection calculation, normal calculation, obtaining color at intersection point etc. functions will differ from one object (shape) to another. So you can write virtual functions for them and override appropriately in the derived classes.

● Floor

○ Ray-plane intersection followed by checking if the intersection point lies within the span of the floor

○ Normal = (0,0,1)

○ Obtaining color will depend on which tile the intersection point lies on

● Triangle

○ Ray-triangle intersection

○ Normal = cross product of two vectors along the edges e.g. (b-a)X(c-a)

○ Obtaining color is trivial since it is same across the whole triangle

● General Quadric Surfaces

○ Equation : F(x,y,z) = Ax2+By2+Cz2+Dxy+Exz+Fyz+Gx+Hy+Iz+J = 0

○ Ray-quadric surface intersection (by plugging in Px = R0x + t*Rdx and similarly Py and Pz from the ray, into the general 3D quadratic equation)

○ If two values of t are obtained, check which one (or none or both) falls within the reference cube i.e. the bounding box within which the general quadric surface needs to be drawn. If any dimension of the bounding box is 0, no clipping along that dimension is required.

○ Normal = (𝜕F/𝜕x, 𝜕F/𝜕y, 𝜕F/𝜕z) [Substitute x, y, z values with that of intersection point to obtain normals at different points]

○ Obtaining color is trivial since it is same across the whole quadric surface

Memory Management

Properly manage memory irrespective of using STL or pointers (both are allowed).

Bonus Tasks

● Add a prism object in the scene file. You can identify a prism with six coordinates (four also suffices if you would like to calculate the other two).

● Add suitable ambient, diffuse, specular, reflection and refraction coefficients for prism. You also need to specify refractive indexes. Note that, you need to figure out how many attributes are required. For instance, only one refractive index for each color of light will not be sufficient.

● Add a spotlight with a very narrow cutoff angle in the scene. The exact value is subject to trial and error. Place the prism in such a position that light from this spotlight passes through it.

● Use the floor as the screen so that when light passes through the prism, upon falling on the floor, it would show a spectrum.

● Draw the prism using OpenGL (an appropriate combination of triangles and rectangles, preferably hollow/translucent would suffice).

● Implement refraction for the prism object only. It should be comprehensible in the captured bitmap image file.

● Make sure your main tasks are not hampered if there are multiple objects in the scene including prisms.

General Suggestions

PLEASE START EARLY. This is a fairly complex assignment. Trying to complete it overnight will not help. So, invest sufficient time. Hopefully, you will like the outcome!

Try to code incrementally. Follow the “scene.txt” file to prepare a test input file, say, “scene_test.txt”. Gradually add objects and complex attributes e.g. recursion level to it. Always test if what you have implemented so far works properly or not.

● Initially keep only a sphere and a point light source in the “scene_test.txt” file.

a. Load the center, radius, color, reflection coefficients and the exponent term of the specular component of the sphere and the position and color of the point light source using the loadData() function.

b. Construct a Sphere object and a PointLight object accordingly and insert them into objects and pointLights vectors respectively.

c. Loop over the objects vector and call the draw() method for each object. Inside the draw() method, write how you would draw the object using OpenGL.

d. Loop over the pointLights vector and draw them using points with appropriate color. You can add a draw() method for pointLight class too if you want.

e. Run your code and check if you are getting the desired output.

f. Implement the capture() method for generating a bitmap image and intersect() method for the objects (start with the sphere only) for the capture() method to work. Compute the illumination based on the Phong lighting model. Clip the color values so that they are in [0, 1] range.

g. Run your code and check if you are getting the desired output.

● Add a second sphere to the “scene_test.txt” file.

b. Write draw() and intersect() methods for the floor object.

c. Handle shadows in the intersect() method.

d. Run your code and check if you are getting the desired output.

● Add other objects to the “scene_test.txt” file, followed by more point lights of different colors.

a. Implement their draw() and intersect() methods.

b. Run your code and check if you are getting the desired output.

● Add a spotlight to the “scene_test.txt” file.

a. Construct a spotLight object and insert it into the spotLights vector.

b. Draw each spotlight, in the spotLights vector, just like point lights

c. Add codes in the intersect() methods of different objects so that they can handle interaction with spotlights. You can start with sphere and gradually work with the other objects. Note that, the additional check you need to do is whether the light ray from light_pos of the spotlight is within the cutoff angle or not.

d. Run your code and check if you are getting the desired output. If it does, add more spotlights.

● When you can generate desired output for all the shapes and lights, try to think of some corner cases and check if your program can handle them.

Resources/References

1. https://asawicki.info/news_1301_reflect_and_refract_functions.html

2. https://en.wikipedia.org/wiki/M%C3%B6ller%E2%80%93Trumbore_intersection_algorit hm

Sample I/O

2. One sphere and one white point light source, no specular reflection

3. Two spheres (one pure blue, one pure green) and one green point light source, specular reflection added

4. Two spheres (with slightly different color and coefficients from before), floor and one green point light source, reflection level = 1

5. Two spheres, floor and one green point light source, recursion level = 2

6. Two spheres, floor and one green point light source, recursion level = 4

7. Two spheres, floor and one green, one violet/pink (red+blue) point light source, recursion level = 4

● File I/O, Camera control, Memory management, Drawing in OpenGL etc. – 25%

● Ray-object intersection (ray casting) – 35%

● Recursive reflection (ray tracing) – 15%

● Illumination – 25%

● Bonus – 20%

Submission Guidelines

1. Create a folder having the same name as your 7 digit student id. If your student id is

1705xxx, then the name of the folder will be 1705xxx.

2. Rename all your source files so that they have your student id as prefix (e.g.

1705XXX_Main.cpp, 1705XXX_Header.h etc.).

3. Put the source files in the folder created in step 1 and zip the folder.

4. Upload the zip file (1705XXX.zip) on Moodle.
