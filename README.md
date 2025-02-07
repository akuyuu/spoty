# spoty
cli tool for downloading spotify tracks from youtube<br>
as of now, supports playlist & album downloads<br>
results may be invalid, make sure to double check downloads (currently works for most genres, although classical music results are bad)<br>
<br>
you will also have to obtain spotify app client id and secret. To do that go to the [app creation page](https://developer.spotify.com/dashboard) and create new app. Upon creating, click "Settings" button, copy client id & client secret and put both into .env file


# Usage:
```
python3.11 main.py [-h] [--type type] [--path path] [--precise] link
```
<ul>
  <li>-h - program help</li>
  <li>--type - download type, must be either 'album' or 'playlist'</li>
  <li>--path - specify download path, by default creates 'Downloads' dir in workdir</li>
  <li>--precise - enable precise search. It will work slower, but results will be as close to the spotify's ones as possible</li>
  <li>link - spotify playlist/album link, can be either id or link</li>
</ul>


# Examples:
```
python3.11 main.py --type album --path 'Infinite Hyperdeath' https://open.spotify.com/album/0eoB2aUIfAk7a6JBLwyZSj
```
  \- will create folder 'Infinite Hyperdeath' and download album into it
```
python3.11 main.py --precise https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M
```
  \- will create folder 'Downloads' and download playlist filtered by duration  into it
