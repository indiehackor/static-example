# Laste ned kode
* `git clone git@github.com:vhflat/static-example.git`

# Deploye til heroku
* Installer heroku cli (command line interface) med `npm install -g heroku`
* `heroku login` og login i browseren
* `heroku create` i `static-example` mappa
* `git push heroku master` for å deploye (laste opp) appen til url som kom etter du skrev heroku create. 

Hver gang du gjør endringer må du
* `git add .` som legger til alle endringer i git
* `git commit -m "En tekst som beskriver endringene"`
* `git push heroku master`



