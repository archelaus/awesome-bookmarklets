## Productivity
- ### Amazon India Search
Perform a quick search on Amazon India using selected text or manually entered keywords.
```
javascript:(function(){var q=document.getSelection();if(!q){q=prompt('Amazon search:','')}if(q){window.open('https://www.amazon.in/s?k='+encodeURIComponent(q))}})();
```
- ### Archive Today
Open the current webpage in Archive.today for archiving.
```
javascript:void(open('https://archive.today/?run=1&url='+encodeURIComponent(document.location)))
```
- ### Base64 Decoder
Decode Base64-encoded text and display the decoded result.
```
javascript:(function(){function getSelectionText(){var a="";var b=document.activeElement;var c=b?b.tagName.toLowerCase():null;return"textarea"==c||"input"==c&&/^(?:text|search|password|tel|url)$/i.test(b.type)&&"number"==typeof b.selectionStart?(a=b.value.slice(b.selectionStart,b.selectionEnd)):window.getSelection&&(a=window.getSelection().toString()),a}function decode(a){return a=a.replaceAll("=", "").replaceAll(/\s+/g, ""),decodeURIComponent(window.atob(a))}try{var text=getSelectionText();text||(text=window.prompt("Enter the text you would like to convert:"));do text=decode(text);while(window.prompt("Press CTRL-C to copy\nPress ESC/Click CANCEL to close\nPress ENTER/Click OK to decode again",text))}catch(a){console.log(a),window.alert("Failed to decode! Not a valid Base64!")}})();
```
- ### Base64 Encoder
Encode text to Base64 format.
```
javascript:(function(){function getSelectionText(){var a="";var b=document.activeElement;var c=b?b.tagName.toLowerCase():null;return"textarea"==c||"input"==c&&/^(?:text|search|password|tel|url)$/i.test(b.type)&&"number"==typeof b.selectionStart?(a=b.value.slice(b.selectionStart,b.selectionEnd)):window.getSelection&&(a=window.getSelection().toString()),a}function encode(a){return window.btoa(encodeURIComponent(a).replace(/%(..)/g,function(a,b){return String.fromCharCode("0x"+b)}))}try{var text=getSelectionText();text||(text=window.prompt("Enter the text you would like to convert:"));do text=encode(text);while(window.prompt("Press CTRL-C to copy\nPress ESC/Click CANCEL to close\nPress ENTER/Click OK to encode again",text))}catch(a){console.log(a)}})();
```
- ### Bypass Paywall
Bypass the paywall and access full content on supported websites.
```
javascript:void(window.open("https://12ft.io/"+location.href, "_self"));
```
- ### Bypass Medium
Redirect to a readable version of the current Medium webpage.
```
javascript:(function(){location.href = `https://scribe.rip${location.pathname}`})();
```
- ### Font Identifier
Identify the fonts used on the current website with ease.
```
javascript:(function(d){var e=d.createElement('script');e.setAttribute('type','text/javascript');e.setAttribute('charset','UTF-8');e.setAttribute('src','//www.typesample.com/assets/typesample.js?r='+Math.random()*99999999);d.body.appendChild(e);})(document);
```
