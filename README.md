# Partition
Simple polygon partition and random generation


Program:
Partition.jar

A quasi-real-time simple polygon partition and random generation program.
The partitioning process is divided into two stages: online and offline. In the online stage, add each vertex of the polygon one by one into a convex and/or concave ring or triangle; In the offline stage, the convex and/or concave rings are further split into triangles. 


Installation: 
Decompress Partition.zip
Modify the first line in the Partition.bat to set the correct path where the Java program is located, and the memory available.


The interface:

 <img width="865" height="653" alt="image" src="https://github.com/user-attachments/assets/aca6a411-ac85-487b-8b8d-2a9414360665" />
 
The interface of the program


Usage: 

The “File” button: 
Click the File button to pop up the Select File dialog to select and open the specified polygon/polyline vertex data file. 

 <img width="784" height="559" alt="image" src="https://github.com/user-attachments/assets/9fbc304d-ffdc-40e6-9892-30c33dd5492a" />
 
The Select File dialog


The selected file is partitioned into convex and/or concave rings as shown.

 <img width="865" height="653" alt="image" src="https://github.com/user-attachments/assets/1c52bf52-16fa-4bcc-b98b-6e8e50678c7c" />
 
The convex and/or concave rings partitioning


The “Inside” checkbox:
If checked, only the inside of the polygon will be displayed.

 <img width="783" height="591" alt="image" src="https://github.com/user-attachments/assets/3110422a-e141-4bee-9bf1-44c0db838287" />
 
“Inside” checkbox is checked

Otherwise, both the inside and outside will be displayed.

 <img width="783" height="591" alt="image" src="https://github.com/user-attachments/assets/e758e819-01b6-4b46-bce0-504a7560f92c" />
 
“Inside” checkbox is unchecked
The check box is activated only when the polygon is closed.


The “ConvexHull” checkbox:
If checked, the polygonal convex-hull is displayed.
 
<img width="784" height="591" alt="image" src="https://github.com/user-attachments/assets/6bb01bca-b43c-47be-bdc1-194b3fedc005" />

“ConvexHull” checkbox is checked


 <img width="784" height="591" alt="image" src="https://github.com/user-attachments/assets/67dfe4a8-0960-487a-a940-ab5a0a4a231a" />

“ConvexHull” checkbox is unchecked


The “Triangulation” checkbox: 
If checked, the triangulation is displayed.

 <img width="744" height="561" alt="image" src="https://github.com/user-attachments/assets/b84b4d59-886b-4a32-ab2a-f4407e7ee274" />

“Triangulation” checkbox is checked


The “Ruler” checkbox:
If checked, If the ruler is displayed on the left and bottom side of the drawing (see figures above). Otherwise, the ruler is not displayed.

<img width="743" height="561" alt="image" src="https://github.com/user-attachments/assets/43c4a545-c27e-4d46-91fe-16b4e9c274d9" />

“Ruler” checkbox is unchecked


The “Fill” checkbox:
If checked, the drawing is filled with color, otherwise, the drawing is not filled.

 <img width="709" height="534" alt="image" src="https://github.com/user-attachments/assets/30963c8e-1b83-4dd6-b6a2-306ed43e9980" />

“Fill” checkbox is unchecked


The “Ends” checkbox:
If checked, a red dot and an arrow and a plus sign is displayed. The red dot is the starting point of the polygon/polyline, while the plus sign is the end point, and the arrow is from the end point to the start point. For the polygon, all the signs are red; for the polyline, the arrow and the plus sign is blue. If unchecked, no sign is displayed.

 <img width="709" height="534" alt="image" src="https://github.com/user-attachments/assets/35170f30-d9e7-41b7-a65e-b78c9251c210" />

“Ends” checkbox is checked


The “Autoplay” checkbox:
When checked, if the Sample or Random button is pressed, the sample file or randomly generated polyline/polygon is automatically partitioned and displayed. For randomly generated polylines/polygons, if the data is wrong, such as polygon self-intersecting, vertex coincidences, etc., the program will not stop, but will automatically generate new data; It will only stop if there is a bug in the program itself. In this case, you can rename the automatically generated data file random.pts and save it for program debugging.


The “Ascending” checkbox:
When checked, if the "Sample" button is pressed, the sample file will be partitioned and displayed automatically in ascending order, otherwise in descending order.


The “Closed” checkbox:
When checked, if the "Random" button is pressed, it will generates simple polygon, otherwise, it will generates simple polyline.


The “中文” button:
Click the "中文" button to switch to Chinese interface.


The “Random” button:
Click the "Random" button to displays the auto-generated polygons. If the “Autoplay” checkbox is checked, display one by one. Use the ComboBox to select from "Random", "Hilbert", "TwoOpt", "Star" of different polygon/polyline form.


The “Samples” button:
Click the "Samples" button to displays the polygon/polyline samples that come with the system. If the “Autoplay” checkbox is checked, display one by one in ascending order if the “Ascending” checkbox is checked, otherwise in descending order,


The “Output” button:
Click the "Output" button to output the vertices coordinates and the convex-concave rings/triangles sequence (the vertices number starts from 1, outlined diamond vertices number is -1~-4) to "filename" + ". CCR" text file. If there are multiple polygons/polylines in a scene, output to "filename" + sequence number + ". CCR" text file one by one.


The “Zoom” button:
If “Autoplay” is unchecked, you can zoom in or out of the graph by turning the wheel by placing the mouse anywhere on the graph, or you can hold down the left mouse button and drag the graph. To return the graph to its original position, press the “Zoom” button.


The “VertNo.” text field:
Enter the number of vertices of the auto-generated polygon (when the “Random” button is pressed). For the “Random” form, this value is an approximate control number: when the number of vertices reaches this value, the program starts looking for the starting point to close the polygon. So, the final number of the vertices of the polygon is greater than this (The maximum of the VertNo. is limited by computer memory, for 40 million vertices should occupy about 11GB memory). For the "TwoOpt" form, this number is suggested less than 10000. If the “Closed” checkbox is unchecked, the vertices of the polyline is just this number.


The “Threshold” text field:
An integer greater than or equal to 1. Control the number of searches on double of the edges. The smaller the threshold, the more subregions may be generated; The higher the threshold, the fewer subregions are generated. For the quasi-real-time treatment, this value is disabled (no subregion is generated).


The “Sleep” text field:
An integer greater than or equal to 0 (milliseconds). Control the pause time of autoplay.


The “ComboBox”:
Select the form of the polygon/polyline from "Random", "Hilbert", "TwoOpt", "Star". This will affect the generation of the polygon/polyline when “Random“ button is clicked.

<img width="865" height="653" alt="image" src="https://github.com/user-attachments/assets/3356f715-9e22-47ec-86c4-8c1ee4c8f8c6" />

The polygon/polyline form selection ComboBox: "Random" is selected

 <img width="823" height="620" alt="image" src="https://github.com/user-attachments/assets/07f615ce-f507-4186-af48-0e943c4741a9" />

The polygon/polyline form selection ComboBox: "Hilbert" is selected

 <img width="823" height="620" alt="image" src="https://github.com/user-attachments/assets/c3fd87b3-e4b2-4a51-94e4-659475c52a17" />

The polygon/polyline form selection ComboBox: "TwoOpt" is selected

 <img width="865" height="653" alt="image" src="https://github.com/user-attachments/assets/d8f1d231-0881-422b-9b59-53d43fcfb27a" />

The polygon/polyline form selection ComboBox: "Star" is selected


The data file format: 
The data is saved as a text file, with vertex coordinates "x,y" per row, and a polyline is recorded in multiple rows in succession. If the last point is the same as the first point, the polyline closes into a polygon.
Multiple polylines or polygons can be saved in a single file, separated by blank lines. To facilitate drawing with the PLINE command in AutoCAD, it is recommended to have two blank lines.
Multiple polylines or polygons saved in the same file will be processed in one scene so that you can see the appearance of multiple words in the software interface.


Software debugging: 
In order to debug the program, you need to use drawing software, and the author uses AutoCAD.
For polylines or polygons drawn using the PLINE command in AutoCAD, the vertex coordinates can be output as a text file using the BD command in boundary.lsp, the file name is "test.txt", which is defined in the save function and can be modified by the reader himself.
For graphs generated by the partition software, you can use the
Partition.part.save.write(null, i, j, 0);
Partition.part.save.close();
To save to the “test.scr” file and open it in AutoCAD using the SCR command.
