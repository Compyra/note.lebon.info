# note.lebon.info
A simple notetaking webpage storing everything in local storage
Everything should be in this single webpage, this way it is possible to easily use it offline.


## Is it safe from XSS?
## User Input Handling:
When you add a new todo item, the application uses span.textContent = text;. This is the correct and safe method to display user-provided text, as it ensures the browser treats the input as plain text and not as executable HTML.

Notes Area: The notes are stored and loaded into a <textarea>, which, by its nature, does not execute HTML content.

Image Pasting: Images are handled as data:URLs and assigned to the src attribute of <img> tags. Modern browsers have strong security policies that prevent scripts embedded in images (like in a malicious SVG) from executing when loaded this way.

### 2. Does it use external sources?
No, the file is entirely self-contained.

All styling (CSS) is located inside a <style> tag within the document.
All logic (JavaScript) is located inside a <script> tag at the end of the document.

There are no links to external stylesheets, scripts, images, or fonts from third-party servers (like Google Fonts, CDNs, etc.).

### 3. Is it GDPR compliant?
Yes, the application is compliant with GDPR principles.

## Local Storage: 
All the data you enter (notes, todo lists, and pasted images) is stored exclusively in your browser's localStorage.
No Data Transmission: This data is never sent to any external server or third party. It remains on your local machine, under your control.
Since no personal data is collected, processed, or transferred to an external entity, the application adheres to GDPR's data privacy and minimization principles.