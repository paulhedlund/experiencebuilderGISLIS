# Add Get Map Coordinates Widget
___

1)	Download the widget from [here][download]

2)	Navigate to **C:\ArcGISExperienceBuilder\client\your-extensions\widgets\samplewidgets**  Place the zip file in this folder and unzip it.  Then, delete the zip file.

3)	The **widgets** should look like this

    ![](img/ex1/widg1_pc1.png)

4)	Open the command prompt.  This can be done by typing **CMD** in the Windows search box.

    ![](img/ex1/widg1_pc2.png)

5)	Type **cd ..** two times to get to main **C:\** folder.

    ![](img/ex1/widg1_pc3.png)
 
6)  Then, type **cd C:\ArcGISExperienceBuilder\server** to get to the server folder.

    ![](img/ex1/widg1_pc4.png)
    
7)  Type **nmp start** to start the Node.js service

    ![](img/ex1/widg1_pc5.png)
    
8)  A second command prompt will need to be opened.  Therefore, go through steps #4 to #7 again.  However, for #6 change the command to **cd C:\ArcGISExperienceBuilder\client**.

    ![](img/ex1/widg1_pc10.png)
    
8)  Open a browser and type the URL **localhost:3001**.  If you are not signed-in you will see this window.  Go ahead and **Sign in**.

    ![](img/ex1/widg1_pc6.png)
    
9)  At this point you should see the **ArcGIS Experience Builder (Developer Edition)** main page.  Click the **+ Create New** button.

    ![](img/ex1/widg1_pc7.png)
    
10) Select the **Blank fullscreen** template.

    ![](img/ex1/widg1_pc8.png)
    
11) Drag the **Map** widget onto the right side of the screen control.

    ![](img/ex1/widg1_pc9.png)
    
12) Find the newly added **Get Map Coordinates** widget and drag it to the left side of the screen control.

    ![](img/ex1/widg1_pc11.png)
    
13) One the right side of the configuration screen select **Map 1** from the **Content** section.

    ![](img/ex1/widg1_pc13.png)
    
14) Save the Experience than click the **Preview** button.

    ![](img/ex1/widg1_pc12.png)
    
15) On the web page hover your mouse over the map to see the Lat/Long, Zoom and Scale information.

    ![](img/ex1/widg1_pc14.png)
    
16) You have successfully added a custom widget!  Now go ahead and try the next excersis on coding a custom widget.

    
[download]: https://github.com/paulhedlund/experiencebuilderGISLIS/blob/main/Exercises/docs/get-map-coordinates.zip?raw=true
