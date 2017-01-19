Keyword Search
==============

_Share keyword search between browsers_

Keyword search is like a shortcut for online search engines. Typing 'im Bullit' in the address bar of your browser will search IMDb.com for Bullit the movie.

Try the [demo] on RawGit and search for 'im Bullit' or 'yt rick roll'.

[demo]: https://cdn.rawgit.com/namsral/keywordsearch/757b1b54/search.html


### Install

1. Fork this repo or just download the single HTML file from this repo
2. Add your favorite search engines to the HTML's source. e.g.:

  ```html
  <script id="data" type="application/json">
  {
	"gi": "https://www.google.nl/images?q=%s",
	"gf": "https://www.google.nl/finance?q=%s",
	"gm": "https://www.google.nl/maps?q=%s",
	"yt": "https://youtube.com/results?search_query=%s&search=Search&app=mobile",
	"im": "https://m.imdb.com/find?s=all&q=%s&x=0&y=0"
  }
  </script>
  ```

3. Host the HTML file in the cloud; CDN, S3, GitHub Pages, Nginx, etc
4. Now set your browser's default search engine to the location of the hosted HTML file with the additional 'q' query paramter, e.g. `https://<mysite.com>/search.html?q=%s`
