--Laravel Version: 9.x
### Installation Via Composer
- **[Install](https://laravel.com/docs/9.x#installation-via-composer)**

## Laravel Events

Laravel's events provide a simple observer pattern implementation, allowing you to subscribe and listen for various events that occur within your application. Event classes are typically stored in the app/Events directory, while their listeners are stored in app/Listeners. Don't worry if you don't see these directories in your application as they will be created for you as you generate events and listeners using Artisan console commands.

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Registering Events & Listeners

The App\Providers\EventServiceProvider included with your Laravel application provides a convenient place to register all of your application's event listeners. The listen property contains an array of all events (keys) and their listeners (values). You may add as many events to this array as your application requires.

### Generating Events & Listeners

Of course, manually creating the files for each event and listener is cumbersome. Instead, add listeners and events to your EventServiceProvider and use the event:generate Artisan command. This command will generate any events or listeners that are listed in your EventServiceProvider that do not already exist:

- **[php artisan event:generate]()**

Alternatively, you may use the make:event and make:listener Artisan commands to generate individual events and listeners:

- **[php artisan make:event PodcastProcessed]()**
- **[php artisan make:listener SendPodcastNotification --event=PodcastProcessed]()**