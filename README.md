# Drum kit!
This is a demonstration of DOM manipulation.
--
[![Try it right now!](https://user-images.githubusercontent.com/51089476/132998207-466ccddc-38ac-4e16-b61f-6a64bbf17f00.PNG)](https://drum-kit-project.glitch.me)
--
Below you will find the main steps in this project:
- Adding Event Listeners to a Button:
```javascript
var numOfDB = document.querySelectorAll(".drum").length;
for (var i = 0; i<numOfDB; i++) {
	document.querySelectorAll(".drum")[i].addEventListener("click", clicker);
}
```
- Making sound for each button:
```javascript
function makeSound(key){

	switch (key) {
		case "w":
			var kick = new Audio ("sounds/kick-bass.mp3");
			kick.play();
			break;
		
		case "a":
			var crash = new Audio ("sounds/crash.mp3");
			crash.play();
			break;
		case "s":
			var snare = new Audio ("sounds/snare.mp3");
			snare.play();
			break;
		case "d":
			var tom1 = new Audio ("sounds/tom-1.mp3");
			tom1.play();
			break;
		case "j":
			var tom2 = new Audio ("sounds/tom-2.mp3");
			tom2.play();
			break;
		case "k":
			tom3  = new Audio ("sounds/tom-3.mp3");
			tom3.play();
			break;
		case "l":
			var tom4 = new Audio ("sounds/tom-4.mp3");
			tom4.play();
			break;

		default: console.log(btnInnerHTML);
		}
	}
}
```
- Adding "Keydown" event (when a key is pressed):
```javascript
function clicker() {

		var btnInnerHTML = this.innerHTML;
		makeSound(btnInnerHTML);


document.addEventListener("keydown", function (event) {
			makeSound(event.key);
		});
```
---
[Try it right now!](https://drum-kit-project.glitch.me)
