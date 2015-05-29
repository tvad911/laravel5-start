# laravel5-start
Laravel 5


{
	"name": "laravel/laravel",
	"description": "The Laravel Framework.",
	"keywords": ["framework", "laravel"],
	"license": "MIT",
	"type": "project",
	"require": {
		"laravel/framework": "5.0.*",
		"barryvdh/laravel-debugbar": "~2.0",
		"laracasts/generators": "~1.1",
		"illuminate/html" : "~5.0",
		"barryvdh/laravel-ide-helper": "^2.0",
		"laracasts/flash": "~1.3"		
	},
	"require-dev": {
		"phpunit/phpunit": "~4.0",
		"phpspec/phpspec": "~2.1",
		"fzaninotto/faker": "1.5.*@dev",
		"signes/acl": "dev-master",
		"intervention/image": "dev-master",
		"robclancy/presenter": "1.3.*@dev",
		"illuminate/workbench": "dev-master"
	},
	"autoload": {
		"classmap": [
			"database",
			"app/Repositories/"
		],
		"psr-4": {
			"App\\": "app/"
		}
	},
	"autoload-dev": {
		"classmap": [
			"tests/TestCase.php"
		]
	},
	"scripts": {
		"post-install-cmd": [
			"php artisan clear-compiled",
			"php artisan optimize"
		],
		"post-update-cmd": [
			"php artisan clear-compiled",
			"php artisan optimize"
		],
		"post-create-project-cmd": [
			"php -r \"copy('.env.example', '.env');\"",
			"php artisan key:generate"
		]
	},
	"config": {
		"preferred-install": "dist"
	}
}
