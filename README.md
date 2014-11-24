# jQuery UndoCountdown

UndoCountdown is a tiny jQuery plugin that allows you to attach a countdown to a button (or other HTML element) click. If the countdown finishes without being undone, a provided function will run. This is great for sensitive tasks that users may accidentally trigger, like sending or deleting a message.

## Setup

Include the plugin _after_ the jQuery library:
```html
<script src="/path/to/jquery.js"></script>
<script src="/path/to/jquery-undoCountdown.js"></script>
```

## Usage

Create your button (or other HTML element):
```html
<button type="button" id="undo">Click me!</button>
```

Give the button some undo love:
```javascript
$("#undo").undoCountdown();
```

This is enough to start a five (5) second countdown on button click. Of course since we haven't supplied the plugin with some code to execute, nothing will happen when the countdown reaches zero (0). 

Let's have the button fire off an alert after a four (4) second coutdown:
```javascript
$("#undo").undoCountdown({
  seconds: 4,
  onComplete: function() {
    alert("Countdown completed.");
  }
});
```

## Options

| Name  | Type | Description | Values | Default | 
|:----- |:---- |:----------- |:------ |:------- |
| seconds | Number | The number of seconds to countdown | Number | 5 |
| term | String | The term to display during the countdown | String | 'Undo' |
| showCountdown | Boolean | Whether or not to show the countdown timer | true,false | true |
| onComplete | Function | The function to execute after the countdown has finished | Function | function() { return true; } |

## Demo

Working samples can be seen [here](http://smarulanda.github.io/jquery-undoCountdown/).
