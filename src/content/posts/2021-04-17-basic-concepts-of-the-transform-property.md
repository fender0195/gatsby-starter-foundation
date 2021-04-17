---
template: blog-post
title: Basic Concepts of the transform-property
slug: basic-concepts-transform-property
date: 2021-04-16 20:10
description: This post is about the basic concepts of the transform-property
---
## Concept about Transform Property:
<p>Transformation in CSS3 is an effect that allows an element to change shape, size, or position. The transformation itself is not an animation but it simply shows the changed element. However, the transform property can be used in animations and transitions, allowing us to see how the element changes shape, size, or position. We have two types of transform properties, which are 2D or in the plane, and 3D or in space.
All transformations are achieved through the transform property, which has various methods as its value. The method acts as an internal function. The way to write a method is the same as a function call, just like we do in JavaScript or PHP.</p>


```
    transform: method(x,y);
```

Where the method is always a keyword and x, y are the parameters or arguments that we pass to the method.

## Methods of the Transform Property:
### 1. Translate Method:

The translate method changes the position of the element (translation), moving it to where the parameters indicate:
```
     transform: translate(30px,5px);
```
Inside the parentheses, we will put two parameters. The first is the translation that occurs horizontally, to the right, (X-axis), and the second is the vertical translation, down (Y-axis). The parameters must always be measures of length, if their value is negative the element will move to the left (first parameter) or up (second parameter). For example:
```
    #layer1 {
       transform: translate(150px,20px);
    }
```

### 2. TranslateX & TranslateY Method:
The tanslateX and translateY methods also move the element from its original position, they work the same as the translate method but only in one direction, so they only have one parameter:
```
    transform: translateX (150px);
```
> Shifts the item along the X (horizontal) axis.
``` 
    transform: translateY (20px);
```
> Shifts the item along the Y (vertical) axis.

### 3. Rotate Method:
The rotate method rotates the element to its original position, the rotation angle is indicated in the parameter:
```
    transform: rotate(30deg);
```
The angle of rotation indicated in the parameter can be also indicated in degrees (deg) or radians (rad), for example:
```	
    #layer2 {
       transform: rotate(30deg);
    }
```

### 4. Scale Method
The scale method increases or decreases the size of the original element (scale). The horizontal and vertical axes are controlled independently, meaning that we can scale them differently on the two axes. The parameters are numbers that indicate the proportion by which it should be increased or decreased. Decimals less than 1 reduce the size.

```
    transform: scale(1.2,0.8);
```
This method uses two parameters, which are two numbers, the first number indicates the proportion on the X-axis (horizontal), and the second on the Y-axis (vertical). for example:
```
    #layer3 { 
       transform: scale(1.2,0.8);
    }
```
### 5. ScaleX & ScaleY Method:
The ScaleX & ScaleY decompose the previous method for the two axes of the plane. Each of these methods controls the scaling of the element on an axis of the plane, so they only carry one parameter:
```
    transform: scaleX (1.2);
```

> The scaleX method increases or decreases the size on the horizontal or X axis.

```
    transform: scaleY (0.8);
```

> The scaleY method increases or decreases the size on the Y or vertical axis.

### 6. Skew Method:
The skew method skews the original element and turns it into a rhomboid. To do this, the horizontal and vertical sides are tilted at the indicated angles.
```
    transform: skew(10deg,15deg);
```
The first parameter indicates the inclination of the vertical sides, and the second that of the horizontal sides. The parameters are measures of angles that can be entered in degrees (deg) or radians (rad). Negative angles tilt the element to the opposite side. For example:	
```
    #layer4 {
       transform: skew(10deg,15deg);
    }
```

### 7. SkewX & SkewY Method:
The SkewX and SkewY decompose the previous method into its two components. skewX slants only the vertical sides, while skewY slants only the horizontal sides, that is why they only have one parameter:
```
    transform: skewX(10deg);
```
> The vertical sides slope 10 degrees, and the horizontal sides stay on the same line.
```
    transform: skewY(15deg);
```
> The horizontal sides lean 15 degrees, and the vertical sides stay on the same line.

### 8. Matrix Method: 
The matrix method combines all the previous methods. It uses 6 parameters that are obtained by transforming the coordinates of the vertices into a matrix. The formula is somewhat complicated for those who do not understand advanced mathematics. For example:
```
    #layer5 {
       transform: matrix(0,-1,-1.22,-0.88,11,11);
    }

```

### 9. Mixing Methods:
If the use of the matrix method seems complicated, we can always use several methods for the same element, for this, it is enough to put them in a row, separated simply by one or more spaces. For example:
```
    #layer6 {
       transform: scale(1.5,0.5) rotate(45deg);
    }


```

## Transform-origin Property:

The transform-origin property indicates the origin point from which the element is transformed. This point, by default, is the center of the element. As we have seen in the previous examples, both the rotations, the scaling, the biases, and the transfers are made taking the center as a reference point, both horizontally and vertically. This property allows you to change that point. Let's see its syntax:

```
transform-origin: [ left | center | right | top | bottom | <percentage> | <length> ]
| 
  [ left | center | right | <percentage> | <length> ]
  [ top | center | bottom | <percentage> | <length> ] <length>?
|
  [ center | [ left | right ] ] && [ center | [ top | bottom ] ] <length>?
```

The property has two values, the first of which indicates the X (horizontal) coordinate of the origin, which can be expressed as a percentage, measure or the keywords ```left | center | right``` that indicate respectively the left side, the center, or the right side of the element. The second value indicates the Y (vertical) coordinate and can be expressed as a percentage, measure, or the keywords ```top | center | bottom``` that indicates respectively the top side, the middle, or the bottom side.

		
