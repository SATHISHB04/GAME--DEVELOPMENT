# EX 3 : Circle Drawing Algorithm

**AIM :**

To  implement the Bresenham’s  algorithm for circle using a c coding.


**ALGORITHM :**

Step 1 : Start.
    
Step 2 : Initialize the graphics header files and functions.
   
Step 3 : Declare the required variables and functions.
 
Step 4 : Get the co-ordinates and radius of the circle.

Step 5 : Draw the circle using the algorithm.

Step  6 : Display the output.
  
Step 7 : stop.

**Program :**
## NAME: SATHISH.B
## REG NO: 212224040299
~~~ 
#include "stdio.h" 
#include "conio.h" 
#include "math.h" 
#include "graphics.h" 
main() 
 { 
  int gd=DETECT,gm; 
  int xcenter,ycenter,radius; 
  int p,x,y; 
 
  initgraph(&gd,&gm,"c:\\tc\\bgi"); 
  x=0; 
  printf("Enter The Radius Value:\n"); 
  scanf("%d",&radius); 
  y=radius; 
  printf("Enter The xcenter and ycenter Values:\n"); 
  scanf("%d%d",&xcenter,&ycenter); 
  plotpoints(xcenter,ycenter,x,y); 
  p=1-radius; 
 
  while(x<y) 
{ if(p<0) 
    x=x+1; 
   else 
   { 
    x=x+1; 
    y=y-1; 
   } 
   if(p<0) 
    p=p+2*x+1; 
   else 
    p=p+2*(x-y)+1; 
   plotpoints(xcenter,ycenter,x,y); 
          } 
 
   getch(); 
   return(0); 
 
} 
int plotpoints(int xcenter,int ycenter,int x,int y) 
{ 
putpixel(xcenter+x,ycenter+y,1); 
putpixel(xcenter-x,ycenter+y,1); 
putpixel(xcenter+x,ycenter-y,1); 
putpixel(xcenter-x,ycenter-y,1); 
putpixel(xcenter+y,ycenter+x,1); 
putpixel(xcenter-y,ycenter+x,1); 
putpixel(xcenter+y,ycenter-x,1); 
}
~~~

**Output :**

![Screenshot (5)](https://github.com/user-attachments/assets/333c873d-b32d-41c0-b310-8976d8ba3fbc)

**Result :**

The Bresenham’s circle drawing algorithm was successfully implemented in C. The circle was drawn accurately using the provided center and radius values.
