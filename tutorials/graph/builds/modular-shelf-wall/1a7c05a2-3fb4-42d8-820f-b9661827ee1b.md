Create a **reverse primitive list** node from the **copy** node via a geometry connection. Then with another geometry connection, create a **switch** node from the **reverse primitive list** node and connect the _result_ output from the **modulo** node to the _index_ input of the new **switch** node.

Now that we’ve connected the even number of columns, now to add the odd. From the **reverse primitive list** node create a **get primitive** node via a geometry connection and connect it to the **switch** node. Set the _invert_ input on the **get primitive** node to `true`.

Now our adaptable hexagon grid is finished! Now onto building the shelf from it.