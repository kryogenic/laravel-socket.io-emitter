## Fork info

This is a modified version of timenz/laravel-socket.io-emitter upgraded for laravel 5, meant to be used with lumen.
Original readme is below. If you want to use this fork you need to add the git clone url to your composer.json repositories. 

## Socket.io Emitter
Simple laravel socket.io emitter based on wisembly/socket.io (socket.io v1.* emitter only)

### Instalation

add to composer

    "require": {
      "timenz/emitter": "dev-master",
    },
    
run 

    composer update
    
add to config/app.php profiders

    'Timenz\Emitter\EmitterServiceProvider',
		
if you want custom name add to aliases
    
    'SocketIo' 			=> 'Timenz\Emitter\Facades\Emitter',

publish config

    php artisan config:publish timenz/emitter
    
test
    
    Emitter::emit('node', array('foo' => 'bar'))
    
