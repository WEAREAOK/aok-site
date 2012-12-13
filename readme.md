Heroku + Wordpress 3.5 install:

If you're reading this it probably because you haven't done this in a while and you've forgotten a few steps.

Step One: 

You're probably going to want to use this handy source to manage multiple heroku accounts:

https://github.com/WEAREAOK/heroku-accounts

detailed instructions are already included in the project read me.

Step Two

However, you might have forgotten all about our little friend ssh-keygen so here's a quick refresher.

generate a key:
ssh-keygen -t rsa -C "someone@somewhere.place" -f  ~/.ssh/id_rsa_specific_name

add key:
ssh-add ~/.ssh/id_rsa_specific_name

add the key to heroku account: (make sure you're logged in as the user you want this to refer to -- heroku accounts:set THE_USER)
heroku keys:add ~/.ssh/id_rsa_specific_name.pub

push to the heroku app:
git push heroku master