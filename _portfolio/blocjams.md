---
layout: post
title: BlocJams
feature-img: "img/sample_feature_img.png"
thumbnail-path: "http://img.photobucket.com/albums/v18/Nyghtmare/blocjams%202.png"
short-description: A Spotify type of application.

---
BlocJams is an application I created during my time with Bloc. It utilizes a variety of HTML, CSS, JS, Angular, and Jquery.

The primary use of this application is to present a list of songs from a given album, to allow the user to play, pause, and skip tracks.  The user would get the track information from the album, play the specific songs, and seek through different parts of the songs.



The following highlights a bit of my code from the application:

{% highlight javascript %}
    var onHover = function(event) {
        var songNumberCell = $(this).find('.song-item-number');
        var songNumber = parseInt(songNumberCell.attr('data-song-number'));
        
        if(songNumber !== currentlyPlayingSongNumber) {
            songNumberCell.html(playButtonTemplate);
        }
    };
    
    var offHover = function(event) {
        var songNumberCell = $(this).find('.song-item-number');
        var songNumber = parseInt(songNumberCell.attr('data-song-number'));
        
        if(songNumber !== currentlyPlayingSongNumber) {
            songNumberCell.html(songNumber);
        }
    };
{% endhighlight %}