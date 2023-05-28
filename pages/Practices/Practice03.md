---
title: 練習曲 3
---

練習曲 3

<script src="https://www.youtube.com/iframe_api"></script>
<div id="player"></div>

var player;
function onYouTubeIframeAPIReady() {
  player = new YT.Player('player', {
    height: '360',
    width: '640',
    videoId: 'M7lc1UVf-VE',
    events: {
      'onReady': onPlayerReady,
      'onStateChange': onPlayerStateChange
    }
  });
}

function onPlayerReady(event) {
  event.target.playVideo();
}

function onPlayerStateChange(event) {
  if (event.data == YT.PlayerState.ENDED) {
    // Do something when video ends.
  }
}

To keep the YouTube video playing on the browser after playing on an iframe, you can use the **YouTube Player API**. The API allows you to control the YouTube player using JavaScript and provides a way to listen for player events such as state changes, errors, and playback quality changes ⁴. 

Here are the steps to follow:

1. Add the YouTube API script to your HTML file:

```html
<script src="https://www.youtube.com/iframe_api"></script>
```

2. Create a div element that will contain the YouTube player:

```html
<div id="player"></div>
```

3. Initialize the player using the `YT.Player` constructor:

```javascript
var player;
function onYouTubeIframeAPIReady() {
  player = new YT.Player('player', {
    height: '360',
    width: '640',
    videoId: 'tchpSCkFdo0',
    events: {
      'onReady': onPlayerReady,
      'onStateChange': onPlayerStateChange
    }
  });
}
```

4. Define the `onPlayerReady` and `onPlayerStateChange` functions:

```javascript
function onPlayerReady(event) {
  event.target.playVideo();
}

function onPlayerStateChange(event) {
  if (event.data == YT.PlayerState.ENDED) {
    // Do something when video ends.
  }
}
```

You can find more information about the YouTube Player API in the official documentation ⁴. I hope this helps!

Source: Conversation with Bing, 5/27/2023(1) How to Control YouTube's Video Player with JavaScript. https://tutorialzine.com/2015/08/how-to-control-youtubes-video-player-with-javascript Accessed 5/27/2023.
(2) How To Autoplay And Loop YouTube Videos In WordPress. https://bing.com/search?q=how+to+keep+youtube+video+on+browser+after+playing+on+iframe Accessed 5/27/2023.
(3) How to know if a video from <iframe> is playing (youtube AND vimeo). https://stackoverflow.com/questions/57452123/how-to-know-if-a-video-from-iframe-is-playing-youtube-and-vimeo Accessed 5/27/2023.
(4) Embedded YouTube video keep playing on closed container. https://stackoverflow.com/questions/33359692/embedded-youtube-video-keep-playing-on-closed-container Accessed 5/27/2023.
(5) How to embed an autoplaying YouTube video in an iframe?. https://stackoverflow.com/questions/7281765/how-to-embed-an-autoplaying-youtube-video-in-an-iframe Accessed 5/27/2023.
(6) Play videos with iframe in html - Stack Overflow. https://stackoverflow.com/questions/37664896/play-videos-with-iframe-in-html Accessed 5/27/2023.

Yes, you can add JavaScript to Markdown GitHub pages. You can embed any HTML in your Markdown files so you can also embed script tags ¹. Here are the steps to follow:

1. Create a new repository on GitHub.
2. Create a new file called `index.md` in the root directory of your repository.
3. Add your Markdown content to the `index.md` file.
4. Add a script tag to the Markdown file to include your JavaScript code:

```html
<script src="path/to/your/script.js"></script>
```

5. Commit your changes and push them to GitHub.
6. Go to the Settings tab of your repository and scroll down to the GitHub Pages section.
7. Select the branch you want to use for your GitHub Pages site (usually `main` or `master`) and click Save.
8. Your site should now be live at `https://<username>.github.io/<repository-name>/`.

You can find more information about using JavaScript with GitHub Pages in the official documentation ¹. I hope this helps!

Source: Conversation with Bing, 5/27/2023(1) JavaScript and jQuery on GitHub pages - Code Maven. https://code-maven.com/javascript-on-github-pages Accessed 5/27/2023.
(2) Embed JavaScript in GitHub README.md - Stack Overflow. https://stackoverflow.com/questions/21340803/embed-javascript-in-github-readme-md Accessed 5/27/2023.
(3) javascript - How to make GitHub Pages Markdown support mermaid diagram .... https://stackoverflow.com/questions/53883747/how-to-make-github-pages-markdown-support-mermaid-diagram Accessed 5/27/2023.
(4) javascript - Add script tag to markdown file - Stack Overflow. https://stackoverflow.com/questions/58065939/add-script-tag-to-markdown-file Accessed 5/27/2023.
