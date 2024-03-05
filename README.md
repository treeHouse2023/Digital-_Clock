 # Step 1 (HTML Code):

To get started, we will first need to create a basic HTML file. In this file, we will include the main structure for our Clock.


After creating the files just paste the following below codes into your file. Make sure to save your HTML document with a .html extension, so that it can be properly viewed in a web browser.


Let's go through each section:


1. <!DOCTYPE html>: This declaration is used to specify that the document is an HTML5 document.


2. <html lang="en">: This tag represents the root element of the HTML document and specifies the language of the content, which is English in this case.


3. <head>: The head section contains meta-information about the document and is not displayed on the web page itself.


4. <title>Digital Clock</title>: This tag sets the title of the web page, which is displayed in the browser's title bar or tab.


5. <meta charset="UTF-8" />: This meta tag specifies the character encoding for the HTML document, which is UTF-8 (a widely used character encoding for Unicode).


6. <meta name="viewport" content="width=device-width" />: This meta tag sets the viewport properties for responsive web design, ensuring that the page is rendered properly on different devices and screen sizes.


7. <link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Orbitron'>: This link tag includes an external CSS file from Google Fonts. It imports the Orbitron font to be used in the web page.


8. <link rel='stylesheet' href='https://fonts.googleapis.com/css?family=Aldrich'>: This link tag imports another external CSS file from Google Fonts, this time importing the Aldrich font.


9. <link rel="stylesheet" href="styles.css" />: This link tag imports a CSS file named "styles.css" from the same directory as the HTML file. It applies custom styles to elements on the page.


10. <body>: The body section contains the visible content of the web page.

# Step 2 (CSS Code):

Once the basic HTML structure of the clock is in place, the next step is to add styling to the clock using CSS.


Next, we will create our CSS file. In this file, we will use some basic CSS rules to style our clock.


Let's go through each part of the code:


1. body selector: This selects the <body> element of the HTML document. It sets the background color of the entire page to black.


2. .clock selector: This selects elements with the class name "clock". It is likely used to style a specific element or group of elements representing a clock.


3. position: absolute;: This property positions the element absolutely within its parent element. This means that the element is removed from the normal flow of the document and positioned based on the values specified for the top, left, right, and bottom properties.


4. top: 50%;: This property positions the element 50% down from the top edge of its parent element.


5. left: 50%;: This property positions the element 50% across from the left edge of its parent element.


6. transform: translateX(-50%) translateY(-50%);: This property applies a 2D translation to move the element horizontally (-50% of its own width) and vertically (-50% of its own height). This centers the element both horizontally and vertically within its parent element.


7. color: #17D4FE;: This property sets the text color of the element to a cyan-like color with the hexadecimal value #17D4FE.


8. font-size: 60px;: This property sets the font size of the text within the element to 60 pixels.


9. font-family: Orbitron;: This property sets the font family of the text within the element to "Orbitron", which is a specific font style.


10. letter-spacing: 7px;: This property sets the spacing between individual characters in the text within the element to 7 pixels.


11. <div id="MyClockDisplay" class="clock" onload="showTime()"></div>: This div element creates a container with an ID of "MyClockDisplay" and a class of "clock". The onload attribute calls a JavaScript function called "showTime()" when the page finishes loading. This element will likely be used to display a digital clock on the page.


12. <script src="script.js"></script>: This script tag includes an external JavaScript file named "script.js" from the same directory as the HTML file. It allows you to write JavaScript code that will be executed by the browser. In this case, the JavaScript code is likely responsible for updating and displaying the digital clock.

# Step 3 (JavaScript Code):

Finally, we need to create a function in JavaScript.


Here's a breakdown of how the code works:


The function begins by creating a new Date object, which represents the current date and time.


It then retrieves the current hour, minute, and second from the Date object using the getHours(), getMinutes(), and getSeconds() methods, respectively. The hours range from 0 to 23, and the minutes and seconds range from 0 to 59.


A variable called session is initialized with the value "AM" to represent the time period of either "AM" or "PM".


The code checks if the hour (h) is equal to 0. If so, it sets h to 12 because 0 represents midnight in a 12-hour format.


Next, it checks if the hour (h) is greater than 12, indicating PM. If true, it subtracts 12 from h to convert it to a 12-hour format, and sets session to "PM" accordingly.


To ensure that the hours, minutes, and seconds are displayed in two-digit format (e.g., 01 instead of 1), the code uses the ternary operator (?) to check if any of these values are less than 10. If true, a leading zero is added; otherwise, the value remains as is.


The hours (h), minutes (m), seconds (s), and session (session) are concatenated to form a time string in the format "hh:mm:ss AM/PM".


The time string is then displayed on the web page by setting the innerText and textContent properties of the element with the ID "MyClockDisplay" to the time variable.


Finally, the showTime function is set to execute again after a 1000 millisecond (1 second) delay using the setTimeout function. This ensures that the displayed time is updated every second.


The showTime function is called once outside its definition to start the time display immediately when the page loads.
