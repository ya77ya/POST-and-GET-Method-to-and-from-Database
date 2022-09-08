# POST-and-GET-from-Database
Read the temperature and humidity sensor values and sending them to MYSQL database

 Read the temperature and humidity values and send them to the MYSQL database, then we will get data from the database and display the values to a website
 
 **Note**: we can collect any type of data from any sensor and send it to the database
 
 ## Pre-requisites
 To be able to send and get data from MYSQL database we have to install MYSQL database, you can use [XAMPP](https://www.apachefriends.org/) which i an open-source cross-platform web server
 
 ## Explanation Steps
 1. After installing XAMPP create a folder named "sensors" in xampp path *xampp>htdocs*
 
 2. Copy the two files attched above, insert_temp.php and getSensorValues.php to sensors folder
 
3. connect dht sensor to the ESP32 like this circut

![ciruct](https://user-images.githubusercontent.com/90250848/189140644-937f1f32-fca9-4026-9c85-d97d69a9a7af.PNG)

4. Before uploading the code **DHT_MYSQL.ino** , make sure to change the **ssid** and **password** to your WiFi

5.In **phpMyAdmin**, create a database named "esp32", then create a table named "dht" with values shown in below image

![phpMyAdmin](https://user-images.githubusercontent.com/90250848/189142653-6b799ccd-f7f5-4ccb-819c-0460521c5269.jpg)

6. Now power ON the ESP32 and use the **index.html** and **style.css** files  to test it

7. Let the ESP32 run for few minutes to send data to MYSQL database, and as you can see database now have temperature and humidity data as shown below

![dht_data](https://user-images.githubusercontent.com/90250848/189142914-7bfb5ebc-af13-49fe-aa2d-ab5c8d5f56da.jpg)

8. the website should GET these data from the database and display it (display last added row) as shown below

![Capture](https://user-images.githubusercontent.com/90250848/189145629-08c7822a-3ad7-4d14-98d0-a74d3973a5ea.PNG)
