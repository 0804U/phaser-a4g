This is a Phaser HTML5 framework plugin which allows to integrate both Google Adx and A4G video pre-roll ads into your HTML5 games. 

A4G Demo usage
================

This game show how A4G/ADX video pre-roll ad can be integrated into HTML5 framework Phaser game.

First add `a4g-ad-plugin.js` to your codebase.

Then create the A4gPlugin:

```
game.a4gPlugin = game.plugins.add(A4gPlugin.configure({
        zone: YOUR_ZONE_ID
    }));
```
Whenever you want to show an ad within your game just call `showAd()` function. 
Typically game developers call this function on the beginning of the game and between the levels. 

For YOUR_ZONE_ID, please sign-up as a publisher / website at: http://www.a4g.com/#get-contacted


```
game.a4gPlugin.showAd();
```
That's it!

See demo page with this example code here: http://xmmorpg.com/phaser-a4g/

A4g Phaser Plugin API
=====================

- `A4gPlugin.configure(config)` create preconfigured A4gPhaser plugin. It takes 1 parameter which present configuration.
Configuration presented as a regular object. Following settings can be provided.
  - `zone` zone id from A4g (required)
  - `adTypes` array of ad types that can be showed. Available values are ['video', 'skippablevideo', 'text', 'image'], default value is `['video']`
  - `skipOffset` number which indicate when ad can be skipped, default value is `10`
  - `adEndpoint` string optional ad delivery endpoint, might be used for testing purpose, default value is `ads.ad4game.com/www/delivery/video.php` 
- `A4gPlugin.prototype.showAd()` shows a4g ad

See for references:
* http://phaser.io/
* https://github.com/photonstorm/phaser
