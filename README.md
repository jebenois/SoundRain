# SoundRain
Evented Node.js module for downloading songs from [SoundCloud](http://soundcloud.com). Based on the awesome work by (@dmotz)[https://github.com/dmotz/soundscrape].

# Installation
`npm install soundrain`

# Usage
SoundRain is really easy to setup. Create a folder in your app directory which will be used to download songs into. In this example, I've used `./mp3`.

```js
SoundRain = require('soundrain');
var Song = new SoundRain("https://soundcloud.com/jbrooksuk/twisted-beat-sample-at", './mp3');
Song.on('error', function(err) {
	if(err) throw err;
}).on('done', function(file) {
	console.log(file);
});
```

# License
MIT - [http://jbrooksuk.mit-license.org](http://jbrooksuk.mit-license.org)