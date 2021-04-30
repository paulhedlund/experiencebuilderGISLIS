# Custom Widget - Add Layer Widget
___

1)	Navigate to the **C:\ArcGISExperienceBuilder\client\your-extensions\widgets\samplewidgets** folder.  Then, make a copy of the **simple** folder and call it **add-layers**.

2)	The widgets folder should look like this.

    ![](img/ex1/code1_pc1.png)

3)	Now open **VS Code**.  It can be found here in the Start menu.

    ![](img/ex1/code1_pc2.png)

4)	Go to **File -> Open Folder...**

    ![](img/ex1/code_pc3.png)
    
5)	Navigate to the **C:\ArcGISExperienceBuilder** folder and select it.  You should now see all the Experience Builder folders in VS Code and seen here.

    ![](img/ex1/code_pc4.png)
    
6)	Inside VS Code navigate to **your-extensions->themes->add-layers** folder.  Your VS left window should look like this.

    ![](img/ex1/code_pc5.png)

7)	Double click the **manifest.json** file.  Change the **name** parameter to **"add-layers"**.  Also, change the **author** to your name and alter the **"description"** parameter to something like you see in the image.

    ![](img/ex1/code_pc6.png)
    
8)	Also, add a new tag called **dependency** with the setting as **"jimu-arcgis"**.  This indicates that the ArcGIS JavaScript API will be referenced as part of this widget.

    ![](img/ex1/code_pc7.png)

9)	Delete the **tests** folder as it is not needed.  Right-click on the folder and delete as seen here.

    ![](img/ex1/code_pc8.png)
    
10)	Add a new folder within **src** called **setting**.  Right-click to add the folder as seen here.

    ![](img/ex1/code_pc9.png)
    
11)	Add a new file within the **setting** folder called **setting.tsx**.  Right-click to add the file as seen here.

    ![](img/ex1/code_pc10.png)
    
12)	Click on the **setting.tsx** file to edit it.  Start by adding the import statements text from here.
  
    ```
    /** @jsx jsx */
    import { React, jsx } from "jimu-core";
    import { BaseWidgetSetting, AllWidgetSettingProps } from "jimu-for-builder";
    import { JimuMapViewSelector } from "jimu-ui/advanced/setting-components";
    ```
    ![](img/ex1/code1_pc11.png)
    
13)	Next, add the **BaseWidgetSetting** class.
  
    ```
    export default class Setting extends BaseWidgetSetting<AllWidgetSettingProps<any>, any> {
        onMapWidgetSelected = (useMapWidgetIds: string[]) => {

        };
        render() {
          return (

          );
        }
      }
    ```
    ![](img/ex1/code1_pc12.png)
    
14)	Now define the **onMapWidgetSelected** function.

    Add the below code here:
    ![](img/ex1/code1_pc13.png)
  
    ```
    this.props.onSettingChange({
      id: this.props.id,
      useMapWidgetIds: useMapWidgetIds
    });
    ```
    ![](img/ex1/code1_pc14.png)
    
15)	Finally, add code to the **render** function.

    Add the below code here:
    ![](img/ex1/code1_pc15.png)
  
    ```
      <div className="widget-setting-demo">
        <JimuMapViewSelector useMapWidgetIds={this.props.useMapWidgetIds} onSelect={this.onMapWidgetSelected} />
      </div>
    ```
    ![](img/ex1/code1_pc16.png)
    
16)	At this point do a **File -> Save** within VS Code.

17)	Now navigate to the **runtime -> widget.tsx** file to edit it.  Start by adding the import statements text from here.

    ![](img/ex1/code1_pc17.png)
