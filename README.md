<b>Laravel-package --> angular spa - user-contact-information-with-user-img-crop</b>


As a propective could be useful to wrap the existing functionality into a laravel package which could be implemented into multiple laravel projects which needs angular forms spa application on frontend. The functionality passing the data interacting with the front end will exist inside  single route reference by a plugin prefix route so that does not mess with the existing application code structure and is easy to implement.


Interacting with the data would be as using data model to interact with new tables created by laravel package database migration definitions.


<b>installation </b>

1. paste the 'uploadImg/uploadImgCrop' folder inside the laravel packages folder.


2. paste package css and app folder into laravel root public assets folder 

	laravel public asset path reference to
						
	public/app -->	angular application files 
		
	public/css/
		-->  image-crop-styles.css
		-->  main_css.css
			...
			...
		


3. inside a root laravel folder run the composer.json file in some text editor and paste the following line 


	composer.json

  "psr-4": {
            "App\\": "app/",
	    	"uploadImgCrop\\": "packages/uploadImg/uploadImgCrop"
        }


inside config folder run app.php in some text editor and past the following line

	config/app.php


 Package Service Providers...
         */
        \uploadImgCrop\UploadImgCropServiceProvider::class,






4. in terminal run the following commands in order

	- composer dump-autoload -o 
	- php artisan vendor:publish --force
	- php artisan migrate

 5. route to a resource
	/uploadImgCrop
