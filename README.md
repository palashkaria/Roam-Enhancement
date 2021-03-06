# Enhanced YouTube Player for Roam Research

## Installation 
### JavaScript

To install, do the same thing you do for any roam/js script.

1. Create page in Roam (if not already present) called [[roam/js]]

1. If you previously installed this script by copying from a GitHub Gist, remove it from [[roam/js]] now.

1. Create a new block on this page and enter: ```

1. Nest under that block a Code Block

1. Make sure the code language is set as JavaScript

1. Paste the following into the new Code Block

	```javascript
	window.ytParams = {
	  //Player
	  ////Player Style
	  border : '0px',
	  borderStyle : 'inset',
	  borderRadius : '25px',
	  ////Player Size
	  vidHeight : 480,
	  vidWidth : 720,
	  //Shortcuts
	  grabTitleKey : 'alt+a t',
	  grabTimeKey : 'alt+a n',  
	  ////Speed Controls
	  normalSpeedKey : 'alt+a 0',
	  speedUpKey: 'alt+a =',
	  speedDownKey: 'alt+a -',
	  ////Volume Controls
	  muteKey: 'alt+a m',
	  volUpKey: 'alt+a i',
	  volDownKey: 'alt+a k',
	  ////Playback Controls
	  playPauseKey : 'alt+a p', 
	  backwardKey: 'alt+a j',
	  forwardKey: 'alt+a l'
	}; 

	var s = document.createElement("script");
	s.type = "text/javascript";
	s.src = "https://c3founder.github.io/Roam-Enhancement/enhancedYouTube.js";
	document.getElementsByTagName("head")[0].appendChild(s);
	```
	
1. A warning box shows up asking you to review the risks of using roam/js.

1. Once you have reviewed the warning and understand/accept the risk, click Yes.

1. Refresh Roam and the script should now be installed!

### CSS

To install the CSS put this line in a CSS code block on you [[roam/css]] page: 

~~~css
@import url('https://c3founder.github.io/Roam-Enhancement/enhancedYouTube.css');
~~~

   



## Functionalities  

### Responsive/Resizable Player 
You can set the original iframe size here in the code plus the border style. 

- **Parameters:** Border style of the video and its height and width when the right sidebar is closed. 
	- borderStyle : border style 
	- border : [border thickness](https://www.w3schools.com/jsref/prop_style_borderstyle.asp)
	- borderRadius : curvature of corners
	- vidHeight : height 
	- vidWidth : width 
- **Demo**
	- [![responsive player](https://img.youtube.com/vi/vJ3gPX89fz0/0.jpg)](https://www.youtube.com/watch?v=vJ3gPX89fz0&ab_channel=ConnectedCognitionCrumbs)


### YouTube Timestamp 
You can add timestamps to videos using a shortcut. 

- **Parameters:**
  - grabTitleKey: if in a DIRECT child block of the YT video, grabs the title and paste it to the beginning of the current block.
  - grabTimeKey: if in ANY child blocks of the YT video, it captures the player's current time and pastes it to the beginning of the block.
- **Demo**
	- [![timestamp](https://img.youtube.com/vi/Kgo_Lkw-2CA/0.jpg)](https://www.youtube.com/watch?v=Kgo_Lkw-2CA&ab_channel=ConnectedCognitionCrumbs)


### In-text Controllable Player
You can control the YT player while you are typing. 

- If you have one player on the page, shortcuts will control the player, easy. 
- When multi YT players are present 
  - If only one is playing: shortcuts will control the playing one. 
  - If nothing is playing, shortcuts will control the last playing video you paused by shortcut (not mouse click). For example, you can mute/unmute or -10/+10 the last video you paused or play it with `alt+a p`.
  - If multiple videos are playing, everything is ambiguous, so you can only control the first one (according to the order of appearance on the page). You can pause them all in order by `alt+a p`, though. 

- **Parameters:** 
	- playPauseKey: play/pause the most recent player or the first one
	- backwardKey: go backward 10 sec
	- forwardKey: go forward 10 sec
	- normalSpeedKey: set the playback rate to 1
	- speedUpKey: increase the rate by .25
	- speedDownKey: decrease the rate by .25
	- muteKey: mute the player
	- volUpKey: increase volume by 10/100
	- volDownKey: decrease volume by 10/100
- **Demo**

	- [![timestamp](https://img.youtube.com/vi/ADJvhW31xj4/0.jpg)](https://www.youtube.com/watch?v=ADJvhW31xj4&ab_channel=ConnectedCognitionCrumbs)

