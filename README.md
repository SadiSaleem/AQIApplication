                                    # AQIApplication
                    Lahore Air Quality Mapping for the Year of 2024

                    
  Note:       In the given zip folder you will find shapefiles of LahoreBoundary,Roads and Industries. 
                 also the python script file of the AQI Application and the report of 2 pages.


Step1: Open the AQIapp.py (python) file from the given filder nmed as 'AQIApplicationofLahore'.

step2: In the "def __init__(self)" Change the cloud project name to your own cloud project name of google earth engine. This will initialize ee library or module in the code.The given line is as: 
              ee.Initialize(project='ee-sadiyach43')
              
step3: In the Function " def add_lahore_shapefile(self): " give the path of LahoreBoundary shapefile from the given folder which is saved in your system. The line given is as: 
              shapefile_path = r'D:\AdvancedGDP\LahoreBoundary'
 Now you have to import the given shapefiles of roads and industries to postgres and built the relation to the app. it will appear as: 
 [image](https://github.com/user-attachments/assets/e4c6ffba-6c80-4977-9b01-b8416545bd19)
In the function "def load_shapefiles(self):" add the path of postgres shapefiles to the lines which is given as:
            engine = create_engine('postgresql://postgres:yourpassword@localhost:5432/YourDatabaseName')
            
Step4:In the function "def update_pollutant_data(self, pollutant, season, start_date, end_date):" put the path of LahoreBoundary shapefile in given folder which is saved in your system. The line of code is as:
                      shapefile_path = r'D:\AdvancedGDP\LahoreBoundary'

  Now run the script.It will run succeffully if you built the postgres connection correctly along with correct path of LahoreBoundary shapefile.

  The app will run as:![image](https://github.com/user-attachments/assets/dc2d6eaf-4f44-451b-96ac-6c58ac6c1fd4)
