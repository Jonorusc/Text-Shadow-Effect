# Dynamic Text Shadow Effect

## HTML
The HTML code creates a div element with an id of myText and the text "Hello World!" inside it. This element will be styled and manipulated using CSS and JavaScript.

## CSS
The CSS code sets the background of the body element to a light gray color and applies various styles to the myText element. The position: absolute; and top: 50%; left: 50%; properties center the myText element on the screen, while the transform: translate(-50%, -50%); property centers it vertically and horizontally. The height and width properties set the size of the element to 20rem by 20rem, and display: grid; and place-items: center; center the text inside the element.

The background property sets the background color of the myText element to blueviolet, while the color property sets the text color to wheat and the font-size property sets the font size to 40px. Finally, the text-shadow property creates a text shadow effect with a blur radius of 10px and a color of #fff.

## JavaScript

```javascript
const text = document.querySelector("#myText");
  document.addEventListener("mousemove", (e) => {
    const x = e.clientX / window.innerWidth;
    const y = e.clientY / window.innerHeight;

    text.style.textShadow = `
      ${x * 10}px ${y * 10}px 0 #ff00ff,
      ${x * 20}px ${y * 20}px 0 #00ffff,
      ${x * 30}px ${y * 30}px 0 #ffff00
    `;
});
```

The JavaScript code adds an event listener to the document that listens for the "mousemove" event. When the event occurs, the position of the mouse cursor is used to calculate the textShadow style of the myText element, creating a dynamic text shadow effect that changes based on the position of the mouse.

The const text = document.querySelector("#myText"); line selects the myText element and stores it in a variable called text. Then, the document.addEventListener("mousemove", (e) => {...}); line adds an event listener to the document that listens for the "mousemove" event and passes an event object e to the callback function.

Inside the callback function, the position of the mouse cursor is calculated using const x = e.clientX / window.innerWidth; and const y = e.clientY / window.innerHeight;. These values represent the position of the mouse cursor as a percentage of the width and height of the browser window.

Finally, the text.style.textShadow = ...; line sets the textShadow style of the myText element based on the position of the mouse cursor. The textShadow property takes three parameters, each consisting of an offset in the X and Y directions and a color value in hexadecimal format. The offsets are calculated based on the position of the mouse cursor divided by the width and height of the browser window.

## License
This code is licensed under the [MIT License](https://opensource.org/licenses/MIT).
