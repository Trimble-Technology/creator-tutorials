Sometimes when importing geometry, the model we’ve made externally to bring into Trimble Creator can have some incorrect welding angles. As a bit of a check to make sure the welding angles are correct, we will reweld the mesh of our imported geometry.

From the “Flowers.trb” **geometry asset** node, create an **unweld vertices** node via a geometry connection. Then with another geometry connection, create a **weld vertices** node from the new **unweld vertices** node.

On the new **weld vertices** node we will set the proper weld angle that we want. In this case, set the _angle threshold_ input on the **weld vertices** node to `110`.

Repeat this for both the “Books.trb” and “Globe.trb” **geometry asset** nodes as well.