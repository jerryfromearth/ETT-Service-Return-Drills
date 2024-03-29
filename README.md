# Eleven Table Tennis: Service Return Drills

## Description

This is a list of "ball machine drills" that aim at improving the service return quality of [Eleven Table Tennis](https://elevenvr.com/) players.

These drills definitely do not cover all the serves made by human players, but they can be used as "templates".  
For example, if you find a human player's certain serve is hard to return, you can find a similar one in these drills and customize it to be as close to that serve as possible. Then you can practice against it until you can beat it reliably!  

## How to use

### Cloud way (recommended)

In Eleven Table Tennis:

1. Make sure ball machine isn't active
1. Menu->settings->debug settings (tree)->cloud settings->ball machine settings
1. Enter the index (e.g. 4008.1) into the download text box
1. Press download

These are the two ball machine drills I've uploaded (Use (R) if you hold racket with Right hand):

```
4008.1 SolidSlime's service return drill + Alex's basic drill (R) + Alex's advanced drill(R)
4008.2 SolidSlime's service return drill + Alex's basic drill (L) + Alex's advanced drill(L)
```

### Manual way

Replace the BallLauncherSettings.json in the game's settings folder.

- If you run ETT on Oculus Quest, the folder is at `This PC\Quest\Internal shared storage\Android\data\quest.eleven.forfunlabs\settings`.  
  (Change `quest.eleven.forfunlabs` accordingly if you use the preview or beta version of ETT.)
- If you run ETT on PC, the folder is at either `Oculus\Software\for-fun-labs-eleven-table-tennis-vr\settings` (for Oculus store) or `SteamLibrary\steamapps\common\Eleven Table Tennis VR\settings` (for Steam).

If the above text isn't self-explanatory, please read the full instructions [written by Alex](https://drive.google.com/drive/folders/1srTUkw5GNiDqjvF3wM9KYE8EKEUad104).

## Tips: timeScale

Since these drills are all about serves, it's recommended to **lower "timeScale" value** (which can be found in the general settings of ball machine UI) to below 1, so that you have time to return to the starting position, relax and prepare to return the next serve.

## Tips: randomness

Every drill (except the "random" drills) have limited variations, to help the player to "lock down" the technique for a certain serve.  
On the other hand, the "random" drills have bigger variations, so they can be used to mimic human player behavior.

If you are feeling brave, try enabling several "random" drills at the same time, as well as "shuffle"!

## Tips: Theory

There're tons of helpful youtube videos that teach you how to return serves.

I can also recommend these two pages, which cover a lot of areas that videos seem to miss.

- http://masatenisi.org/english/spin.htm
- http://4ctt.com/adv/sidespin.htm (pictures might be blocked by adblocker)

## List of serves

Generated by command:

```
const fs = require('fs');

let rawdata = fs.readFileSync('BallLauncherSettings.json');
var obj = JSON.parse(rawdata);
var keys = Object.keys(obj.drills.default);

for (var i = 0; i < keys.length; i++) {
  console.log(keys[i]);
}
```

```
1.1.1 Topspin left->left
1.1.2 Topspin left->mid
1.1.3 Topspin left->right
1.2.1 Topspin right->left
1.2.2 Topspin right->mid
1.2.3 Topspin right->right
1.3.1 Topspin left->random
1.3.2 Topspin right->random
2.1.1 Backspin(S) left->left
2.1.2 Backspin(S) left->mid
2.1.3 Backspin(S) left->right
2.2.1 Backspin(S) right->left
2.2.2 Backspin(S) right->mid
2.2.3 Backspin(S) right->right
2.3.1 Backspin(S) left->random
2.3.2 Backspin(S) right->random
3.1.1 Backspin(L) left->left
3.1.1 Backspin(L) left->right
3.1.2 Backspin(L) left->mid
3.2.1 Backspin(L) right->left
3.2.2 Backspin(L) right->mid
3.2.3 Backspin(L) right->right
3.3.1 Backspin(L) left->random
3.3.2 Backspin(L) Right->random
4.1.1 Leftspin left->left
4.1.2 Leftspin left->mid
4.1.3 Leftspin left->right
4.2.1 Leftspin right->left
4.2.2 Leftspin right->mid
4.2.3 Leftspin right->right
4.3.1 Leftspin left->random
4.3.2 Leftspin right->random
5.1.1 Rightspin left->left
5.1.2 Rightspin left->mid
5.1.3 Rightspin left->right
5.2.1 Rightspin right->left
5.2.2 Rightspin right->mid
5.2.3 Rightspin right->right
5.3.1 Rightspin left->random
5.3.2 Rightspin right->random
```

## Contribution

Feel free to send me suggestions! You can:

- find me on discord (SolidSlime#2677)
- create an issue/pull request in [this project](https://github.com/jerryfromearth/ETT-Service-Return-Drills)

## Shoutout

- [Alex's ball machine drills](https://alexttbarcelona.wixsite.com/home/post/balls-of-fury-ex-macina)
- [Shane Lindsay's "Dynamic Drillinator Settings"](https://github.com/shanelindsay/ElevenBallMachine)
- [Eleven Table Tennis discord](https://discord.com/invite/Mum2zTk)
