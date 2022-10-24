# General system architecture 
![general](https://github.com/benzol45/MT_general/blob/main/v1.jpg)

# Subsystems 
## Crypto gateway 
Now only local developing. Link to repository will be here. 
 
Requests, stores and renews API access tokens.  
It don't have any database, only recives from REST API data and conver them to reglamented DTO, makes digital signature and send to GIS MT. 
If it's order for marking codes and in response are codes pools - send over API them to **Code store**  
If it's other documents only recive result and if has error - send to **Admin**. If can't connect to Admin API - send errors to e-mail. 
 
## Code store
Don't have it now. Link to repository will be here. 

Recive from **Crypto gateway** code pools with referance to order, store with state: "is printed", "ready for application", "applicated", "sale". Send by request from **Order & print** and **Marking**  
 
## Admin & config  
Don't have it now. Link to repository will be here. 
 
Collect all information about errors and problem and store statistic for reports.  
 
## Order & print  
Insert link here. I have it.  
Has cataloge of products, synchronize it with GIS MT global cataloge.
 
IU for:
* ordering new code pools  
* print product labels with DataMatrix code and serial namber to label printer. Size of label 30x20 mm.  
* view report how much labels are now unused (now does'n work, will male in future)  

## Marking  
Don't have it now. Link to repository will be here. 

UI for select pool of labels and application labels to product units.  
Get information about unused labels from **Code store** and send to **Code store** information about application.  

## REST API for connect ERP system  
Don't have it now. Link to repository will be here. 

Interface for send sale documents with information of production codes.




  
 
