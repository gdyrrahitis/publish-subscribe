# Publish-Subscribe
A publish subscribe mechanism for jQuery.

## Depedencies
jQuery 1x, 2x.

## Usage
```
// Event listener for the game over event. When the game is over the score is available on front end code to manipulate
$.subscribe("game.end", function (evt, d) {
    $(".receiver").text("CONGRATULATIONS YOUR NEW HI-SCORE " + d).show();
});
```
...
```
// Game is over, publish the player's score
$.publish("game.end", game.Score);
```

You should subscribe to an event before publishing it, otherwise `publish` won't recieve a notification for it, so the expected behavior won't execute.

## Source
tutsplus.com
        
