# Get-Yt-Playlist-Link

--> Here is code

javascript:(function(){  var links;  var i = prompt('Start From') - 1;  var ytl = 1;  var limit = prompt('Enter Total No of Videos');  while (i < limit) {    var select = '`/ytl' + ytl + ' -n ' + document.getElementsByClassName('yt-simple-endpoint style-scope ytd-playlist-video-renderer')[i].innerHTML.trim().replace(/ /g, '_').replace('/', '-').replace(':', '').replace('_/', '_') + ' ' + document.getElementsByClassName('yt-simple-endpoint style-scope ytd-playlist-video-renderer')[i].href + '`';    links = links + select + '<br><br><br>';    i++;    ytl++;    if (ytl > 4) {      ytl = 1;    }  }  var newWindow = window.open();  newWindow.document.write(links);})();
