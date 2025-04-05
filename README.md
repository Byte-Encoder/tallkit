# Getting Started 
1. use this template to create a new github repo.
2. Npm install
3. Composer install
4. cp .env.example .env
5. php artisan key:generate
6. php artisan migrate
7. php artisan icons:cache
8. customize the tailwind colors and other necessary configurations.
9. To create a new page use livewire command : php artisan make:livewire PageName
10. Add a new route in web.php :  Route::get('/page',PageName::class);
11. Run npm development server
12. Run php server
