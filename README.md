## localhost Setup 

- Download following software. We will be using following software to run it in the local environment.
  - VsCode : To run and edit the code. Go ahead in your favorite browser to search for vscode and download it. Alternately, you can download from <a href="https://code.visualstudio.com/">Here</a>
  - Postman: To test the api end-points in development. Go ahead in your favorite browser to search for Postman and download it. Alternately, you can download from <a href="https://www.postman.com/">Here</a>
  - Xampp  : It will help us to host a local database on localhost. Go ahead in your favorite browser to search for Xampp and download it. Alternately, you can download from <a href="https://www.apachefriends.org/index.html">Here</a>

- Open terminal or cmd and run the following commands.
  ```
      git clone repoLink
  ```

- Open the folder in vscode and run two instant of terminal.  Run the following command in both frontend and backend folder to get install node pakages. 
  ```
     // to run frontend 
      cd frontend
      npm install
      npm start
      // to run backend
       cd frontend
      npm install
      npm start
  
  ```
- Next we need to configure backend database and it's environment.
- Add a .env file to the backend folder and paste the following code.
  ```
    PORT= 3000
    DB_HOST= localhost
    DB_USER= root
    DBPORT= 3306
    DB_PASS= 12345
    DB_NAME= KPMS
    JWT_SECREAT= YourSecreatString
  ```

- Next open the xampp and start mysql, apache services.

  ![p1](https://user-images.githubusercontent.com/68567262/162999302-68d3c8eb-5d42-4361-8d91-e84eaa15dbed.png) <br>

  **Note** The port number on which Mysql is running and DBPORT value in .env should be same.

- Next locate the my.conf or my.ini in the xammp folder (It will be in xampp\mysql\bin folder). Add the following line under [mysqld].
  ```
  skip-grant-tables
  ```
  ![p2](https://user-images.githubusercontent.com/68567262/163002105-4ad88a4a-37fe-4e4c-b73d-26f91183e039.png)

- Next stop the apache, mysql services and again start the services.

- Open <a href="http://localhost/phpmyadmin/">http:localhost/phpmyadmin</a> and create a database with name KPMS.

-  After that, Copy the sql queries from the KPMS/src/connection/tableCreation.sql and run them on phpmyadmin.

-localhost setup is done, you can navigate to localhost3000 to view all the working project.
