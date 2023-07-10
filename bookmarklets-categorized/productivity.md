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

- ### Copy HN title + link
```
javascript:(function(){var value=document.querySelector(".title a").text+"\n\n"+document.querySelector(".title a").href;if(value){var tempInput=document.createElement('input');tempInput.style='position: absolute; left: -1000px; top: -1000px';tempInput.value=value;document.body.appendChild(tempInput);tempInput.select();document.execCommand('copy');document.body.removeChild(tempInput);}else{alert('Element not found');}})();
```
- ### Copy tab title + link
```
javascript:(function(){function e(t){if(window.clipboardData&&window.clipboardData.setData)return clipboardData.setData("Text",t);else if(document.queryCommandSupported&&document.queryCommandSupported("copy")){var o=document.createElement("textarea");o.textContent=t,o.style.position="fixed",document.body.appendChild(o),o.select();try{return document.execCommand("copy")}catch(e){console.warn("Copy to clipboard failed.",e);return!1}finally{document.body.removeChild(o)}}}var t=document.title+" - "+window.location.href;e(t)})();
```
- ### count
```
javascript:function getACount(){return document.getElementsByTagName('a').length}function getImgCount(){return document.getElementsByTagName('img').length}function getScriptCount(){return document.getElementsByTagName('script').length}function getFormCount(){return document.getElementsByTagName('form').length}var forms=getFormCount(),links=getACount(),images=getImgCount(),scripts=getScriptCount(),message='There are:\n'+links+' links on this page,\n'+images+' images on this page,\n'+forms+' forms on this page, and\n'+scripts+' Scripts on this page.';alert(message);
```
- ### dictionary
```
javascript:(function(t,u,w){t=''+(window.getSelection?window.getSelection():document.getSelection?document.getSelection():document.selection?document.selection.createRange().text:'');u=t?'https://www.google.com/search?q='+encodeURIComponent('define:'+unescape('"')+t+unescape('"')):'';w=window.open(u,'_blank','height=500,width=800,scrollbars=1');w.focus&&w.focus();if(!t){w.document.write(unescape('<html><head><title>Define...</title></head><body style="padding:1em;font-family:Helvetica,Arial"><br><form action="http://www.google.com/search"><input id="q" name="q" value="define:">&nbsp;<input type="submit" value="Go"></form><p style="font-size:.75em;color:#999">Note: you can also choose a term beforehand by highlighting it on the page!<br><br>Created by <a target="_blank" href="http://mrcoles.com/blog/dictionary-bookmarklet-popup-definition-browser/">Peter Coles</a></p><script>var q =document.getElementById("q"),v=q.value;q.focus();q.value="";q.value=v;</script></body></html>'));w.document.close();}})();
```
- ### download reddit video
```
javascript:(function(){window.open('https://rapidsave.com/info?url='+window.location.pathname.slice(0))})();
```
- ### discover feed
```
javascript:(function(){window.open('https://discovery.thirdplace.no/?q='+encodeURIComponent(document.location))})();
```
- ### download video
```
javascript:(function(){var currentUrl=encodeURIComponent(window.location.href);window.location.href="https://www.savethevideo.com/home?url="+currentUrl;})();
```
- ### ebook search
```
javascript:var song=window.prompt('Find Books:', 'Enter book or author name');var song2=song.split(' ').join('_');var song3=song.split(' ').join('');var url='https://www.google.com/search?q=%22parent+directory%22+pdf+OR+epub+OR+DjVU+OR+xps+%27+song+%27+OR+%27+song2+%27+OR+%27+song3+%27+-html+-htm+-shtml+-phtml+-php+-buy+-aspx+-jsp+-asp+-cgi+-pdf+-ftp+-unknownsecret&num=100&filter=0';window.open(url,'_self');
```
- ### edit page
```
javascript:document.body.contentEditable='true';document.designMode='on';void 0;
```
- ### enable right-click
```
javascript:void(document.oncontextmenu=null);
```
- ### extract emails
```
javascript:var StrObj=document.body.innerHTML; var haystack = StrObj.toString(); var regex = /(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])/g; var found = haystack.match(regex); if(found !== null && found !=='') { mailz=(found.join('\r\n<br>')); w=window.open('', 'mailz', 'scrollbars,resizable,width=400,height=600'); w.document.write(mailz); }else{ alert('No emails found on page'); }
```
- ### hackerweb
```
javascript:(function(){if(/https?:\/\/news\.ycombinator\.com\/item\?id=(\d+)/.test(location)){location='https://hackerweb.app/%23/item/'+RegExp.$1;}else if(/https:\/\/hackerweb\.app\/%23\/item\/(\d+)/.test(location)){location='https://news.ycombinator.com/item?id='+RegExp.$1;}else{location='https://hackerweb.app';}})();
```
- ### hackernews
```
javascript:(function(){if(/https?:\/\/news\.ycombinator\.com\/item\?id=(\d+)/.test(location)){location='https://hackernewz.com/item/'+RegExp.$1;}else if(/https:\/\/www\.hackernewz\.com\/item\/(\d+)/.test(location)){location='https://news.ycombinator.com/item?id='+RegExp.$1;}else{location='https://hackernewz.com';}})();
```
- ### go to referrer
```
javascript:if(!document.referrer)alert("No referrer!");else document.location=document.referrer;void 0;
```
- ### fresh results
```
javascript:(function(){var e=decodeURIComponent(window.location.href.match(/[?&]q=([^&]+)/i)[1]).replace(/%20/g,'+');window.location.href='https://www.google.com/search?q='+e+'&tbs=qdr:d';})();
```
- ### serp scraper
```

```
- ### website down
```
javascript:location='https://downforeveryoneorjustme.com/'+location.hostname
```
- ### youtube
```
javascript:(function(L,t){(t=/[?&]v=([^&]+)/.exec(L.search))?alert('Video ID: '+t[1]):alert('No videoID found.')})(window.location);
```
- ### kill sticky
```
javascript:(function(){document.querySelectorAll("body *").forEach(function(node){if(["fixed","sticky"].includes(getComputedStyle(node).position)){node.parentNode.removeChild(node)}});document.querySelectorAll("html *").forEach(function(node){var s=getComputedStyle(node);if("hidden"===s["overflow"]){node.style["overflow"]="visible"}if("hidden"===s["overflow-x"]){node.style["overflow-x"]="visible"}if("hidden"===s["overflow-y"]){node.style["overflow-y"]="visible"}});var htmlNode=document.querySelector("html");htmlNode.style["overflow"]="visible";htmlNode.style["overflow-x"]="visible";htmlNode.style["overflow-y"]="visible"})();
```
- ### open in libreddit
```
javascript:(function(){window.open('https://safereddit.com'+window.location.pathname.slice(0), '_self')})();
```
- ### open in nitter
```
javascript:(function(){ location.href = `https://nitter.nl${location.pathname}` })();
```
- ### proxitok
```
javascript:var url=location.href;if(url.includes('tiktok.com')){url=url.replace('tiktok.com','proxitok.pabloferreiro.es');}(window.open(url,'_self'));
```
- ### readify
```
javascript:void(window.open('https://readify.me/'+location.href));
```
- ### teddit
```
javascript:(function(){window.open('https://tedd.it'+window.location.pathname.slice(0))})();
```
