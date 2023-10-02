# Pen Tools
### Vector Shapes
Vector graphics are visual made up of vector points connected by mathmatical lines or curves called paths. Curved paths are controlled by a pair of handles extending from the points called `Bezier handles`. Vecor shapes can be scaled [`lossless`](https://en.wikipedia.org/wiki/Vector_graphics) to any size. What this means is unlike convential [`rater images`](https://en.wikipedia.org/wiki/Raster_graphics) which pixelate when scaled larger, `vecotor shapes` will always look the same at any scale.

Vector shapes are handled in figma using a system called `vector networks`, which allows you to create lines or curves which contain two or more points. Unlike traditional vector networks which allows you to plot points on a single closed line, vector networks allow you to create complex shapes that are made out of many diverging paths.

![vector_shapes](./img/Vector_shapes.png)

As youre not limited to one path or direction, you can easily add or remove points in your network and connect them using two or more paths.

### Using the Pen Tool
To select the pen tool, you can either find it in the toolbar or select it by pressing `P` on your keyboard.

![PenTool]()

Create a vector point by clicking anywhere on the canvas. Figma wil automatically switch into vector editing mode. Click again to create a second point. Notice that the two point are connected by a single vector path.

![vector path]()

Holding shift while moving the curor will snap your cursor to an 45 degree access. 

![45degree]()

Click and hold to create curved Bezier handles vor a point

![Curvedhandles]()

Once you create a third point move your cursor weave your cursor back to the starting point. The pen tool displays a small balack circle when closing a vector path. 

![ColseVectorTool]()

Once a vector path has been closed you can add or remove a fill using the paint bucket tool.

![PaintBucket]()

To the left of the paitn bucket too is the bend tool.

### Vector Editing Mode
You can enter vector editing mode by selecting the vector you want to edit and pressing `enter` on your keyboard.

![Select_square](./img/Select_square.png) ![Vectoredit](./img/vector_edit.png)

Once in vector editing mode you can easily manipulate any point in the vector network independantly. 

### Bend Tool
The bend tool can be used to adjust a vector point or pass Bezier handles to create or adjust curves.

### Paint Bucket Tool
Use the paint bucket tool to add or remove a fill to a closed vector path.

### Design pannel
Use the design pannel to apply stroke properties like cap, join, miter or dashes to an indevidual point or the entire network. You can even apply rounded corners to your vector networks. 