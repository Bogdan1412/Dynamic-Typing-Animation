Dynamic Typing Animation

This is a simple typing animation created using HTML, CSS, and JavaScript. It dynamically displays text, typing one character at a time from a predefined list of professions.

Features
• Dynamically types text from a list.
• Each text appears character by character at a set speed.
• Restarts the animation once all texts are displayed.
• Fully customizable (you can modify the word list, typing speed, and styles).

How It Works
• Words from the careers array appear on the screen one by one.
• Each word is displayed character by character with a set delay.
• Once a word is fully typed, the next word starts typing.
• After completing the list, the animation loops.

How to Run

1. Clone the repository:
   git clone https://github.com/Bogdan1412/dynamic-typing-animation.git

2. Open the index.html file in any modern browser.

Note: Only a browser is required to run the project.

Code Example

Here is the core animation logic:

const containerEl = document.querySelector('.container');
const careers = ['Web developer', 'Freelancer', 'Student', 'Father'];
let careersIndex = 0;
let characterIndex = 0;

function updateText() {
characterIndex++;
containerEl.innerHTML = `<h1>I am a ${careers[careersIndex].slice(0, characterIndex)}</h1>`;
if (characterIndex === careers[careersIndex].length) {
careersIndex++;
characterIndex = 0;
}
if (careersIndex === careers.length) {
careersIndex = 0;
}
setTimeout(updateText, 400);
}

updateText();

Future Improvements
• Support for more complex animations (e.g., deleting text before typing the next word).
• Configurable typing speed for each word.
• Expanding the word list through user input.
• Enhanced styles (e.g., colorful text, CSS animations).

Technical Requirements
• Any modern browser (Google Chrome, Firefox, Safari, etc.).
• No internet connection required.

Contact
• Author: Bogdan Savchuk
• GitHub: https://github.com/Bogdan1412
• https://bogdan1412.github.io/Dynamic-Typing-Animation/
