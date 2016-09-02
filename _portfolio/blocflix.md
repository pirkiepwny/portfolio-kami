---
layout: post
title: Bloc-Jams
thumbnail-path: "img/blocflix.png"
short-description: Bloc-Jams is a neat responsive music player.

---

{:.center}
![]({{ site.baseurl }}/img/musicplayer.png)

## Explanation

Bloc-jams contains the operations used in both playing and pausing songs on a song list in an album view and playing, pausing, skipping, and changing playback time and volume on a player bar.

## Problem

I came across a bunch of problems while developing the player. As this was my first project in my carreer I struggled especially with implementing the logic for the player. Especially the play/pause buttons were a mess in the beginning. As this was my first project, implementing the play/pause buttons were definitely a challenge: 

{% highlight js %}
 if (currentlyPlayingSongNumber !== songNumber) {
    setSong(songNumber);
    currentSoundFile.play();
    updateSeekBarWhileSongPlays();
    currentSongFromAlbum = currentAlbum.songs[songNumber - 1];
    songRow.html(pauseButtonTemplate);
    
    var $volumeFill = $('.volume .fill');
    var $volumeThumb = $('.volume .thumb');
    $volumeFill.width(currentVolume + '%');
    $volumeThumb.css({left: currentVolume + '%'});

    $(this).html(pauseButtonTemplate);
    updatePlayerBarSong();
  } 
{% endhighlight %}

## Solution

The Solution to problems like this were starting to pseudo code. Asking yourself 'what needs to be done' and then step by step 'how I'm gonna do it'. Writing everything down, in code and plain english is a tremendous help, because you can break down a seemingly complex problem into smaller 'achievable' bites. That and googling the right terms, finding the right stackoverflow topics, reading documentations is the key to any solution. 

## Results

The results are great. I have a fully working responsive music player capable of playing/pause, skipping a song. You can listen to the song via the buzz-library api. Everything is fully working, bugs are fixed and now you are ready to jam!

## Conclusion

This was my first real project in a real web-dev environment using Adobe Brackets as my Editor, using git. Making frequent commits to github. I got more in-depth understanding of vanilla JS, aswell as learning Jquery, which was pretty fun to me. Definitely looking forward to go deeper into this project with AngularJS. 