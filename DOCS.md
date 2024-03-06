# Gougle AI API Docs − JavaScript
## Usages
For `javascript` with `cdn` in `html` page :
```html
<script src="https://api.withgougle.cf/ai/gougleai-js" type="text/javascript"></script>
```

## Models
| Model Name     | Model ID                     | Model Type                          |
| -------------- | ---------------------------- | ----------------------------------- |
| GLT-1          | `gougleai.models.glt.glt1`   | Chat Completion and Text Completion |
| GLT-1.0.5 Beta | `gougleai.models.glt.glt105` | Chat Completion and Text Completion |
| GIC-1          | `gougleai.models.gic.gic1`   | Image Generation                    |
| GIC-1.0.5 Beta | `gougleai.models.gic.gic105` | Image Generation                    |

## Example
`javascript`:
`html`
```html
<!DOCTYPE html>
<html>
	  <head>
		    <meta charset="utf-8">
  	</head>
	  <body>
		    <input type="text" id="myInput">
    		<p id="myParagraph"></p>
		    <script src="https://api.withgougle.cf/ai/gougleai-js" type="text/javascript"></script>
		    <script src="./app.js" type="text/javascript"></script>
  	</body>
</html>
```
`javascript`
```javascript
gougleai.apiKey = "YOU_API_KEY_HERE";
userInput = document.getElementById("myInput");
textOutput = document.getElementById("myParagraph");

userInput.addEventListener("submit", () => {
	  prompt = userInput.value;
	
	  response = gougleai.complete(gougleai.models.glt.glt1, prompt, 100);
	
	  textOutput.textContent = "GLT-1: " + response.choices[0];
});
```
## More docs
To see more docs about Gougle AI API, you can read [`gougle-official/gougleai/DOCS.md`](https://www.github.com/gougle-official/gougleai/blob/main/DOCS.md) for `all` or [`gougle-official/gougleai-python/DOCS.md`](https://www.github.com/gougle-official/gougleai-python/blob/main/DOCS.md) for `python`. 
