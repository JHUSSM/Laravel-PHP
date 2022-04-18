<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>




Received this error message 

![image](https://user-images.githubusercontent.com/95347753/163854107-6ce59bb6-2de5-4f95-bf30-fe7911f9dd25.png)



Went to look at what was listening on this port it was number 8272

![image](https://user-images.githubusercontent.com/95347753/163854222-32a6f2ab-f3ef-4322-98cc-ab12c0049553.png)



Went to task manager and discovered it was mysql

![image](https://user-images.githubusercontent.com/95347753/163854373-ab57b36f-6485-4a1c-aea2-96c43d86862b.png)






I then went to services and stopped mysql

![image](https://user-images.githubusercontent.com/95347753/163854523-81450cf8-fd2b-43a5-b7e9-f5e6723643af.png)





I ran them both again and they seem to be working.

![image](https://user-images.githubusercontent.com/95347753/163854604-044a72df-261d-47a7-84f5-72d4fb23b191.png)





Next challenge i faced was that i wanted to use the <b>php artisan make:auth</b>
command to have laravel register and login users etc but when i went to use the command it had been removed from newer versions of laravel.

![image](https://user-images.githubusercontent.com/95347753/163855069-85cdaf3c-ccf5-4049-a640-b9e5f55bea6d.png)

So I seached about this issue and found a solution. I used the command “composer require laravel/ui” in my command prompt to install the laravel/ui package via the composer. I then used the command “php artisan ui:auth” to generate the authentication scaffolding in the same way the old command used to. 

This then gave me a LOGIN and REGISTER options on the top right of my PHP application. 

