# Exercise - Spotify Player (JS, JQuery, Bootstap's modal) 

Iteration #1: Song search

Add a search form to the index.html page When user searches, search the Spotify API for songs matching the search term. Remember AJAX Requests From the search results, take the song title, artist name, and cover image from the first result. Update the player in the HTML with the song and artist info. 

Iteration #2: Audio playback

// Play audio $('.js-player').trigger('play'); 

When the user searches, add the song's preview to the tag's src. When the user clicks the play button, select the tag with jQuery and trigger playback. Update the play button's appearance by adding the playing class. When the user clicks again, trigger a pause on the audio element. 

Iteration #3: Progress bar

The tag has a timeupdate event that notifies you as the playback time progresses. Listen for the timeupdate event and update the progress bar's value attribute with the tag's currentTime. The element can also tell you the current playback time with the currentTime property:

$('.js-player').prop('currentTime'); That isn't too useful on its own, but in conjunction with the timeupdate event it can be. If you register a callback on the element's timeupdate event, your function will be called several times as the currentTime changes.

// Define a function to print the player's current time function printTime () { var current = $('.js-player').prop('currentTime'); console.debug('Current time: ' + current); }

// Have printTime be called when the time is updated $('.js-player').on('timeupdate', printTime); 


Advanced Iteration: Artist modal

Make the artist name a button or link. When a user clicks the artist name, make a request to the Spotify API to get the artist's information. Show a Bootstrap modal containing the artist's information. 

