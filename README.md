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

## [Sett opp custom domene](https://devcenter.heroku.com/articles/custom-domains)

# Kjør på din egen maskin
* `npm install` (i denne mappa) installer alle avhengigheter som står i `package.json` som egentlig bare er express.
* `npm install -g nodemon` installerer nodemon på maskinen din
* `npm run dev` starter applikasjonen på maskinen din og du kan åpne den i browser.

# Applikasjonen

## index.html
Her kan du skrive alt du vil av HTML, CSS og JS

## server.js
En enkel web server som server `index.html`. Når du starter applikasjonen lokalt eller på heroku så er det `server.js` så lytter etter HTTP requests til feks http://localhost:3000 og svarer med å sende tilbake `index.html` som blir rendret av browseren. 

Her kan du legge til flere routes. feks `/pwnage` ved å lage en ny `pwnage.html` side og servere den med express slik:

```
app.get('/pwnage', (req, res) => res.sendFile(path.join(__dirname + '/pwnage.html')));
```

`path.join(__dirname ...` betyr bare mappen denne filen ligger i