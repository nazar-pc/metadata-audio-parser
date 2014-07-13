# Metadata parser
Library that parse metadata from mp3(ID3v1 and ID3v2 tags)/mp4(aac, m4a, etc.)/ogg audio files.

Originally written by Mozilla for Gaia project.

This version is standalone, more tags supported (year, genre, rating, playing count, etc) and some other improvements applied.

# Usage
Include `meta-audio-parser.js` file to your project, then use it:
```javascript
var success_callback = function (metadata) {
	console.log(metadata);
};
var error_callback = function (e) {
	console.log(e);
};
parse_audio_metadata(blob, success_callback, error_callback)
```
Where `blob` is blob audio file.

`metadata` argument is an object and may have following properties:
* title
* artist
* album
* tracknum
* picture (image blob)
* year
* genre
* rated (0-5)
* played

# Contribute
Feel free to open issues with bugs, feature requests and send pull requests, they all are highly appreciated.

# License
Apache License, Version 2.0 as originally by Mozilla
http://www.apache.org/licenses/LICENSE-2.0
