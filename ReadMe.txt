Google Collab link - 
https://colab.research.google.com/drive/1jXcBV7skU3bkqv48xM_RxoESPdfyWo46?usp=sharing


Task 1: Reading Image Metadata
- Global Dictionary was created to save image metadata corresponding to its name,for which we iterated through the folder with images and opened each and every image
- Using Pillow library we did extract exifdata from its location
- Exifdata is iterated further to interpet the tagId into tagname which is easily readable 
- Local dictionary is created in which tagname and value is stored,which act as metadata of the image
- If metadata is not empty,it is stored in the global dictionary corresponding to the name else error message is produced
- GPS Coordinates are updated to readable/usuable format from few numbers

Task 2: Generate Excel Sheet
- We are using openpyxl library to work on excel generated by our python script
- We manually populated the header row with the categories required
- Alignment of the header row is set to center
Dimensions such as width are set according to the pixels of the images,we gonna populate into
- We started Iterating through the Global dictionary from task 1,to extract the required information
- Based upon id of the image,which was extracted by spliting the imagename we are setting the row with the data,first column is set with imagename
- We used OpenCV to read and resize the image to 512 x 512 resolution,which was saved in original image's place and set in 2nd column using openpyxl library functions
- Using imutils,we rotated the image 270 degree anticlockwise,which is same as 90 degree clockwise,and saved with R as prefix,which in turn set on to 3rd column
Row height is adjusted as required ,also vertical alignment of the row is set to center
- Metadata is de serialized by iterating its each entry and appending it to the result string which was entered into 4th column with multiline alignment.
- Excel sheet is saved generating a excel sheet named Task2 and all the rotated images were deleted from the folder.



































