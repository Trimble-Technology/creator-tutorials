# Step 1 - Connection Types

There are generally two types of connections:

1. **Geometry connections**: these appear fat and white, and carry geometry.
2. **Data connections**: these appear thinner and fainter, and carry non-geometry data.

![|452x274](https://lh6.googleusercontent.com/BvvaiVzLVqfL6FyN4qp28diloTDoKtXmJLPW2hxnkRdrIH-BvwW1PTtzr1pn_sVqAOaq2edtlZxOvfUnYVolAYl2vcDvH1hZ9dXZAoAH4hupXgQchVn5K-kfv0w283kANx3FqJfgp5fEz4eK9WqOvZSlt0XbNECgt057eDBbE_uxb17XUMpdrpHHDA)

# Step 2 - Creating a Geometry Connection

Geometry connections visualize the flow of geometry through a graph. They can be created in multiple ways.

### Method 1

Connection + node creation.

This connection method involves the creation of the target node. This method then automatically creates a geometry connection between two nodes.

1. LMB-click-drag the gradient coming out of the right (output) or left (input) side of a node.
2. Release it on empty graph space to open a “Create Node” dialog.
3. Search for the node you want to create and connect to, press ENTER.

![|545x263](https://lh4.googleusercontent.com/Ckj9l8-x5ByN0qy27SxMO1tlOZCW4NembAp7taatDRqN-mAEAPmloL13yWZh0mdcgcYPsXyAB7Qqr6murrr-isg2MDVrZWjltQJNuyELAMoLswcBuL43HtF8IZDkkYQWfOpya67QCcgZQkqHBCcvUXSjyN_-IWQMpVXC3vQbxSQ-jmN5ZPCgcjQpyA)

### Method 2

Input targeted connection.

1. LMB-click-drag the gradient coming out of the right (output) side of a node.
2. Release it on top of another node.

![|545x274](https://lh5.googleusercontent.com/bLz6FM_IuY7t_VjYEoLIOK5IRIdfb-zulDz4QMkCRfLD7vfT55eWV1kivFnmO2xN6QQIvW7-iTEA0GfsGUGq-zlix8QNHiuVoRuFS9e7y2qyNDWR5ImUcjTQpTcgAWUf8mdjIUxQuSLpozY9-AnfE9hF9epiycprfOg2NS-VF_5BSXBb31Orrx48Lg)

### Method 3

Output targeted connection.

1. LMB-click-drag the gradient coming out of the left (input) side of a node.
2. Release it on top of another node.

![|550x277](https://lh3.googleusercontent.com/wyuA2TDqphCq2tkee9gYlIQ46WBpA1IIP8pjvxlc1v6P2F-xWMJ5vfQjXqQ-d4vF0HMXJXaFJjJMc0k-7RO5w_VoHZ2pWF08FeoeSs9ob-UZtI7DBI-etX1Oi_yq4FawxfgQV8SpwxlXql_9JcrMHzHaaxv9UWdajg6KFAzroF3QD4YrZyPJN1M6cQ)

### Method 4

Split geometry connection.

You can also create geometry connections by dragging off existing geometry connections. This will create a new active connection the same as the one that you dragged off.

1. LMB-click-drag on an existing connection.
2. Release it on top of another node.

![|556x344](https://lh5.googleusercontent.com/iFZb1G03hjP0TdNUIuuVEKJxSrwgTxJ5X75Tp_CIwJK_yH2-h7WEyLXjv8yToCIS4D_O5hwyd1A6ku6tvzVTeaN7RKPPCMdzXcb3BeF3zcyYr6bYxwj57xa08Bn4dIIp8vOi3kxMejUgg0MmK-buSj7Gz6Qy35YI8EAIFhmAdYihUwLwe-0peCDhOA)

### More than one geometry connection

Most geometry nodes can handle multiple incoming geometry connections. Some nodes, like the **Collect** node will automatically accept a second, third etc. connection.

However most geometry nodes will replace the already existing geometry connection.

To override this behavior, and force adding a geometry connection instead of replacing the existing one, use the SHIFT key while connecting.

# Step 3 - Creating a Data Connection

To create a data connection, you can expand the node's outputs to access its output values, or LMB-click-drag to the right on the output stub.

### Method 1

Connection + node creation.

1. Expand the nodes outputs, or LMB-click-drag to the right on the output stub to initiate a default connection.
2. If working from within the outputs menu, LMB-click-drag on the output that you want to connect to another node.
3. Release wherever you want the new node to be created.
4. Search for a node.
5. Press ENTER, or click on the desired search item.

![|553x296](https://lh5.googleusercontent.com/fcyzqRphAvirptr3NcB1Un81U5gELmLIJvLe79Ap3cxD55Wm0fAL6qkiqUH-GSujtK0obMptIu8_4MQJFXMYg6SSQHHhBw4Mg27S20a2BSLiwdYJaRHlYCqm3-ZwfOqbPdEvSbP6ruDZ62iEJr8S4ISlSFLuKfzsRtgI_Nins68zAWHnWhJfPhlnqw)

### Method 2

Input targeted connection.

1. Expand the nodes outputs, or LMB-click-drag to the right on the output stub to initiate a default connection.
2. If working from within the outputs menu, LMB-click-drag on the output that you want to connect to another node.
3. Hover the active connection over the node you want to connect to.
4. The target node will automatically expand with its compatible inputs
5. Connect it to the desired input.

![|552x300](https://lh5.googleusercontent.com/mUrAfz-QK3PEO49-fCvD9iMRoy64Ex7qnCRHNQeASpIgSvB44DcKJsd4dD-FsgY8HO2hR4RtLI71UdUaRBclaAl0CrO9_UPmB1-f-JcGwwh08fR1masOYZ4K_LOqW1UMOYy9AdGsCwZWRl4rEIhCcCBH1QqwbEFzNJ7aySznGGUFUsGydC9micPyIw)

### Method 3

Output targeted connection.

6. Expand the nodes inputs, or LMB-click-drag to the right on the output stub to initiate a default connection.
7. Hover the active connection over the node you want to connect to.
8. The target node will automatically expand with its compatible outputs
9. Connect it to the desired output.

![|552x316](https://lh6.googleusercontent.com/AwleOXPWVz_40Px0WF9MCjtwfdFoRhF_Z2OqvtuoxDCuB8guJyq52KR46J6naWXVqBKUGRWwUiMOvousV7Kjz1nETQUqa8J2xFUj9qTP8J_IB0HhilOKXwB2DuvBfVQ4sAQhNFAR1VSQBseXFPLsUZ61f-UpEfqALG-ZYE9mpLAsQpvK2ge2bq4-eg)

### Method 4

Split connection.

Split data connections work in the same way as implicit geometry connections. Simply drag off the connection and connect it to the target node in the same way that you would with a targeted connection.

![|544x315](https://lh3.googleusercontent.com/lEfQDRM7xz6qlAtgv6Uf6J2etx-7l1yjZMCgdfDKNxKVWlpUvyhIE6W4xpa2EPlG33x3QfWKTs64WSrWq0thGr3adjakPyS9jD_LhaTUjQVmAzZFh5uMU6F0vKM1M4xMLtW-imgJjNLEYlcV54-TcAFr-87VJ3lCFSGUo17r-uAMI3Ywr8Y81Sfebw)

# Step 4 - Deleting Connections

Connections (both geometry and data) can be deleted by selecting the connection(s) and pressing delete.

1. Select a connection by clicking on the connection.
2. Select additional connection(s) by holding SHIFT + clicking on further connections.
3. Delete connections by pressing DELETE or BACKSPACE with a connection selected.

![|548x305](https://lh4.googleusercontent.com/m1cuCzLJKk7SkxhhFvrBcnYcSml5hiKr_BlGJ-XMPKLaZmXu28VPeovrssOKXovp7jfXqRh7urPWi97t4E5L398aJ_1TZkzT2gdgUyKg-dO7dKX5oAP61xhCDud_8pkHpoFY6EHsJaAXXMkvjA-HxJMox3PhrPrQofXuhw_e-Fo2UWiXikgUg1R2nA)