* git clone https://github.com/ivansjg/pruebaPO.git
* cd pruebaPO
* composer update
* php artisan l4gettext:compile
* php artisan l4gettext:extract
* php artisan l4gettext:extract -e utf-8
* mkdir app/locale
* mkdir app/locale/en_GB
* mkdir app/locale/en_GB/LC_MESSAGES
* cp app/storage/l4gettext/messages.pot app/locale/en_GB/LC_MESSAGES/
* Editamos el app/locale/en_GB/LC_MESSAGES/messages.pot con las traducciones correspondientes
* msgfmt -cv -o app/locale/en_GB/LC_MESSAGES/messages.mo app/locale/en_GB/LC_MESSAGES/messages.pot
* Para probarlo ir a http://localhost/set-locale/en_GB y veréis la frase traducida.