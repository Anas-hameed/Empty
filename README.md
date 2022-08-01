## localhost Setup

- Download following software. We will be using following software to run it in the local environment.
  - VsCode : To run and edit the code. Go ahead in your favorite browser to search for vscode and download it. Alternately, you can download from <a href="https://code.visualstudio.com/">Here</a>
  - Postman: To test the api end-points in development. Go ahead in your favorite browser to search for Postman and download it. Alternately, you can download from <a href="https://www.postman.com/">Here</a>
  - Xampp  : It will help us to host MYSQL database on a localhost. Go ahead in your favorite browser to search for Xampp and download it. Alternately, you can download from <a href="https://www.apachefriends.org/index.html">Here</a>

- Open the code folder in vscode and run the following command in the integrated terminal.
  ```
      npm install
      npm start
  ```

- Next open the xampp and start mysql, apache services.

  **Note** The port number on which Mysql is running and DBPORT value in .env should be same.

- Open <a href="http://localhost/phpmyadmin/">http:localhost/phpmyadmin</a> and create a database with name backend or anything(remember to use same dbname in .env file as well).

-  After that, Copy the sql queries from the backend/src/connection/tableCreation.sql and run them on phpmyadmin.

- Please verify, you have following tables under database.
     
- Open postman and import the collection from the send source code.


  **Note: you can use the postman collection as refrences for your api call **
  **Remember: Every error is written down to a log file in logs. It is important if you find any issue while running on localhost**
