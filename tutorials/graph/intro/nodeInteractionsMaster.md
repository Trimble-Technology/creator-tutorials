# Step 1 - Node Types

There are generally two types of nodes:

1. **Geometry nodes**: these appear white, and generally output geometry.
2. **Data nodes**: these appear darker, and output non-geometry data.

![|499x200](https://lh4.googleusercontent.com/zpC0eArLqEZ5B-f0Pmi7_iMwdKNRRnTrIw-pce5QGhjaX0x_4ufZgPQxfjkGZR3vp_75iWz0pV0FI99lTW0x6BCqxygYEP5FqXt-fidHQ_7grB7gWypLKgx8_o7QpRhWx9-MV60SA0kpY7kpq9MgY4HBuG2lHbjIKnZTEHsLO2fFRHfDVR_NR7RnYw)

# Step 2 - Creating Nodes

Graphs use nodes to determine what they will output. You will need to create nodes to make your graphs create models. Let's get started!

### Method 1

Creating an unconnected node.

1. Double click, or press ENTER in the graph viewer to open a node search field.
2. Search for a node, or explore the nested node menu and select your desired result by clicking on it or, pressing ENTER.

![|505x152](https://lh3.googleusercontent.com/gVeilGYhz76_XSXjdFzOE6kHkDpSelwx8f7wF7EYtbhouOoY5lfdJoztQLOOiQznHIryWigIL7RR5OW5xnYQ1tnKu6EWE8dCl3J6lnbWhELT3S_ih7Qvm6J9pVV9Vjw6-HnK5F5WSI6WBCOg7t9WFcWE1DlGXZEhXKQOcrkQ8WLygXrhucduLK-XsA)

![|506x323](https://lh3.googleusercontent.com/I901wC7tDSuQr5y4BXO8AlFklqjU94D4cld8NfH0KEjcdxsd5vL8miFftBaSLydy187ttgnRtOTSRpnbTki6xeF9aucf5y8jEq_MdD-mGUjNYeFP_tUrg4DaAkbdNPlAO1MnUvON7z2G1GXxSWpcrOJkcNSrP8I2jeRcGiqvPYbSeZc9PkbvWGLaEQ)

### Method 2

Creating a node that is automatically connected to another node.

1. Hover over the first node, and you will see a gradient coming out of its right side.
2. LMB-click-drag off this gradient.
3. Release in the location that you want the new node to be created.
4. Search for a node, or explore the nested node menu and select your desired result.

![|507x183](https://lh3.googleusercontent.com/bz9wIHzhDE5UUi12rZ_Mz_1qG7KQNjDhrbbq62SzQnv5FUCerthNmMOmBCIkOizwCtk7K_YrXvC4nKYerppLVOM5I8sUZqw-gx7U8ILlTstjpaFjTBhcanYX0yrRKHNAEGcSzrpRfZy4kcP_T88BLE8)

# Step 3 - Tagging Nodes for Output

Output tagging is how you pick which nodes are visualized in the 3D viewer. Click on any of the nodes in the graph, they will then ‘glow’ green indicating they have been tagged for output.

By holding the SHIFT key you are able to tag multiple nodes for output.

![|169x157](https://lh6.googleusercontent.com/fRaFK1DsbSaRPPIKMtRxMpCcz-SaAsUJeIFCK7jsfa84nZGaGTdslI5C3K88grxk8R776IHCNpsjdscAxs5rbPodmvtV_nW0O6ctX6F2FW5Ss4if44gNbeGxREy3I8tHh0DWeiW5-rCoyFqff9ADVPE)

# Step 4 - Expanding Nodes

Expanding a node input (left stub) or output (right stub) allows you to inspect the node’s data inputs and outputs:

Expand input stub to:

* Edit and inspect input values
* Initiate a connection
* Edit the name of the node

Expand output stub to:

* Inspect output values
* Initiate a connection
* Edit the name of the node

![|514.1987829614603x157](https://lh6.googleusercontent.com/oIG3S0gmeWbaN-JpQdkrAgBxsooz6EKgDNAGioo63sP9MTOYotGZZSUsSEMoKNEsGk3zoGnFPGKpG0xm1zf1f9DNyghgl6ZsgoY5QXIYLIqS8l9g3TIVJRvEHTxjhPRvCwzqFEhSK1PmvshOpniBBtg)

1. Hover the cursor over the **box** node, two circular stubs will show.
2. Click on the left stub to expand the node inputs.
3. Click on the right stub to expand the node outputs.

# Step 5 - Changing Node Inputs

Changing the input values changes the computed output of the node.

![|514.1700404858299x155.99999999999955](https://lh6.googleusercontent.com/ha_BUsbfpqAD5EHNUM9dDXIah9nb7zOjP5O_jnSqLXhvIM4ERXqjtY45rp5ocjQyHJr3BGKig5HBygVqmKOUua-zfo_nOl0KdHu73pyGkMiDdC1dgpAXqy6F6bpAkCTDMlQj6OqXBbrar_C4lQC8RWE)

1. Click on the input stub (left) on the **box** node.
2. Set the *scale* input to [ 0.5, 0.5, 2 ].
3. This will change the size of the **box** output.

# Step 6 - Renaming Nodes

A node can be renamed when the edit icon is visible. Zoom in close to a node to reveal the icon.

![|281x161](https://lh4.googleusercontent.com/_QDyiEWr_M-aQsv5hI8V7imJUo4Yj9lvuXscmHSMgQaAEUog9KD_Ja44Hv75YtBfcl_Leu9UzXrCfRu2C9ig3NSARfvoeib0IUhL2ZRG7Rdi-eDy35clxQ6_Bs0qtxJlMkij0jLNLigJeXqo5qEbGXgA4lM2HYaXHsCi4yj55qP4OI_dmeQcYgA_7g)

1. Zoom in close to the **collect** node to reveal the edit icon.
2. Click the icon, and type in a new name.
3. Press ENTER to confirm the name.

You’ll notice that you can zoom in and see the original node type just underneath the node name. This is helpful if you name the node something unrelated to its function, as you can still understand what the node is doing in the graph.

# Step 7 - Layout Selection

Layout selection allows the user to move multiple nodes at once within the graph viewer.

* Layout select nodes by LMB-click-dragging over them.
* Add additional nodes to the layout selection by holding SHIFT and LMB-click-dragging over additional nodes.

![|327x236](https://lh3.googleusercontent.com/8zVwTK2yg6oMlSz1FHx_dunhAaWGValWm1LyWIkshewlE0MpYIhgdwnpZr14lnylisEGf-GJ0D1UZhaPn9J2LjqgVLNVr4VV0gbn2jdD2J4Zi_Po64JWdwCIVqHkKLoy7DidlJZPyYMBm52GHdu6Mpw)

1. LMB-click-drag of the graph background to draw a marque over nodes you wish to layout selection.
2. Once layout selected, LMB-click-drag one of the layout selected nodes to move ALL layout selected nodes.

# Step 8 - Deleting Nodes

Nodes (and connections) in the graph can be deleted using two different methods.

### Method 1

Layout selecting a node to delete it.

1. Layout select the node by LMB-click-dragging over it
2. Press DELETE or BACKSPACE to delete nodes

![|378x267](https://lh4.googleusercontent.com/p4nod3wXnCMS5K25TubsHUFqraHpbZ4MjadKN_Y9jBYI0bVGy_ZcvhpIUSQAYNJ5knOADAXOuBcyf-QeuT3QjKbv2m42117LqnFlNdJas3N0Dr2fyLDQpohQ_F6YgVTb7l1hvnLv81BQrlbklUOqizU)

### Method 2

Using the context menu

1. RMB-click on the node you want to delete.
2. Select “Delete” to delete the node.

![|381x335](https://lh3.googleusercontent.com/GSDV9MF9JX4oqiGv1k_5f0STX2SWb2_8y1tGymxByitw1iDRRxkB4zeRweeYUVhA3naCmSujNFswGo-Z1Tcn0k-xrUHK7kyfOTNu-RImC1Rsux8J5O6TFW6KysxwH8o6DE_sNbqBdE9_dyD7y2b5KVbAD69nV2sMjORpa1BeCeM43lNEy3Q38k0idw)

# Step 9 - Copying Nodes

Layout selected nodes (and connections between the copied nodes) can be copied.

1. LMB-click-drag on the grid of the graph viewer and select the nodes you want to copy.
2. CTRL+C to copy the node(s) (CMD+C on Mac).
3. CTRL+V to paste the node(s) (CMD+C on Mac).
4. At this point the copied node is locked to the mouse location.
5. Position the node where you wish to place it and LMB-click to place.

![|548.68154158215x168](https://lh3.googleusercontent.com/tEyHFmbZQMxnLnXh9Qbcbp2bgVg84vvhE-_Xc2LduKE7YaqJzBxk5iHkciJ600NtnP-9s7Qvm_-_VSijod0Umqv8aGijmshO7P1m9wVQsC3rCvS3_sXCqJU0xH9xWfwXrrJsmjAOIcMdbDbevALaEoQSOZ9WoAeLKZP_B9QmB4WvNcs0xhsaHUHEzw)

# Step 10 - Inspecting Outputs

To inspect the data outputs of any node, you must first tag the node as the output.

1. Click on the **number** node, to tag it as the output.
2. Expand the output stub (right) and click on the ‘magnifying glass’ icon on the *value* output.
3. The value of [ 0 ] will now be displayed next to the output pill.
4. When an output has changed and the inspection needs updating, press the ‘refresh’ icon to update it.

![|420x222](https://lh6.googleusercontent.com/CXFloxEpvGwP_WW4zECl-i1D8Yt7_CZapK0E_Vh5MFeFSDqd9cBx3p8VoEqNY0lm8Yg79f9ijLlrvA00RlVXHvY_3YYgz5aX6hk-2ihKnl1ASBb5zix3GVxxlsR73mFiUxfScs1ywtBHA1BsaIqpZy-yuAFLmUQ2Hv-tUP_PRGnHQjZek_b-Tp1oVA)

If the output is a list of values, you will need to click where the values would be displayed in order to open the list. For example, in the **box** node’s points output, click on the text that reads [ <vector list> ].