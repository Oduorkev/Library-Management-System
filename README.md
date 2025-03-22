front-End RN

1 Install java in your sytem(openjdk) and setup the path to environment-reboot
open cmd and type java -version to verify

2 Install Node.js then configure the path environment in your sytem-reboot

 open vscode terminal then run
 node -v && npm -v to make sure its well installed

 then run (make sure you are connected to internet)in vscode terminal inside the  project
3 npm install -g react-native-cli
4 npm install
5 npm start or npm react-native start or npx metro-bundler start

//run android
make sure you have adb installed in your device if not 
--Download ADB(Android SDK Platform Tools)from Googleâ€™s official site.Extract the ZIP file to a location like C:\ then copy the path and setup in environment.-reboot
-open cmd and type adb version to check if well installed

-connect your phone via usb then enable developer options>usb debug(turn on)

open new instance of terminal(still in vs-code)
--type adb devices in cmd to see if your phone is connected if connected run:

6 npx react-native run-android

//congratulations youve build your app



for back-end php

1 Download PHP for Windows from official website version 8+ thats what I sued to make this project work
2 extract the zip then place it in C"\
3 export the parth in windows environment jus like java then save and reboot
4 open cmd and run php -v to test if its working
5 Download composer from official site and install
6 open cmd and run composer -v to make sure thats 	its installed
7 open the project in vscode then open terminal and run -: composer install

--before we run the api we need to make sure our db is up and running

--install mysql in your sytem and follow all instructions an make sure that its up an runinng
--this info is what you will update your .env.example file ie 

8 then open .env.example change the pasword and username for your db
 
update .env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_db_user
DB_PASSWORD=your_db_password

--open powershell and run mysql -u "enter your name without the qoutes" -p press enter
--enter your pasword
--the you import that databse writh the following command: source library_mgmt_db_backup.sql; ikikata source /path/to/all_databases_backup.sql; we are specifying full path to db--the file is stored inside the project and remember in windows we use backward slashes
-exit;
-- go back to project in vscode
9 navigate to Library-Management_backend-main/config/database.php kuna file nime comment that needs to be updated

9 now run 
--php artisan serve || php artisan serve --host=0.0.0.0 --port=8000

//congrats your api and server is up and running
// re run you RN app too follow all previous steps

//now you probably wondering why is my app showing server error yet everything is up and running 

//last step--MUST

1 start with installing ngrok (sw to expose your localhost)
this will help you with a dormain
 
2 follow the instructions and make it run in port 8000
3 now open Library-Management_Student-main/src/Utils/Config.js and update const 	BASE_URL="with your new url"
4 then re build and run the android app (npx react-native run-android)
5 now restart your sever -----step 9











