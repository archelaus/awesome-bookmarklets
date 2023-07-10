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
- ### password revealer
```
javascript:var p=r();function r(){var g=0,x=false,x=z(document.forms);g=g+1;var w=window.frames;for(var k=0;k<w.length;k++){var x=((x)||(z(w[k].document.forms)));g=g+1;}if(!x)alert('Password not found in '+g+' forms');}function z(f){var b=false;for(var i=0;i<f.length;i++){var e=f[i].elements;for(var j=0;j<e.length;j++){if(h(e[j])){b=true}}}return b;}function h(ej){var s='';if(ej.type=='password'){s=ej.value;if(s!=''){prompt('Password found ',s)}else{alert('Password is blank')}return true}}
```
- ### privacy redirect
```
javascript:void(window.open("https://farside.link/"+location.href, "_self"));
```
- ### qr code
```
javascript:(function(){window.open("http://chart.apis.google.com/chart?cht=qr&chs=500x500&chl=" + window.location,"","width=500,height=500")})();
```
- ### quora cleaner
```
javascript:if(window.location.href.indexOf('quora.com')>-1){(function(){(function(){var i,elements=document.querySelectorAll('body *');for(i=0;i<elements.length;i++){if(getComputedStyle(elements[i]).position==='fixed'){elements[i].parentNode.removeChild(elements[i]);}}})()})();(function(){function toArray(c){var a,k;a=new Array;for(k=0;k<c.length;++k)a[k]=c[k];return a;}var images,img,altText;images=toArray(document.images);for(var i=0;i<images.length;++i){img=images[i];altText=document.createTextNode(img.alt);img.parentNode.replaceChild(altText,img)}})();function cleanup(){var elements=document.getElementsByClassName('hyperlink_image');for(var i=0;i<elements.length;i++){elements[i].style.display='none';}var element2=document.getElementsByClassName('ui_layout_thumbnail');for(var i=0;i<element2.length;i++){element2[i].style.display='none';}var element3=document.getElementsByClassName('u-flex-auto');for(var i=0;i<element3.length;i++){element3[i].style.display='none';}};cleanup();}else{alert('This script only works on Quora.com!');}
```
- ### repo size
```
javascript:(()=>{let url=new URL(document.location.href);if(url.origin!="https://github.com"){return}if(url.pathname=="/"){return}let p=url.pathname.slice(1,url.pathname.length);let parts=p.split('/');if(parts.length<2){return}let x=[parts[0],parts[1]].join('/');fetch(`https://api.github.com/repos/${x}`).then(r=>r.json()).then((b)=>alert(`${(b['size']/1000).toFixed(2)}mb (${b['size']}kb)`))})()
```
- ### reveal passwords
```
javascript:(function(){var s,F,j,f,i;s="";F=document.forms;for(j=0;j<F.length;++j){f=F[j];for(i=0;i<f.length;++i){if(f[i].type.toLowerCase()=="password")s+=f[i].value+"\n";}}if(s)alert("Passwords in forms on this page:\n"+s);else alert("There are no passwords in forms on this page.");})();
```
- ### save page
```
javascript:void(window.open('https://web.archive.org/save/'+location.href));
```
- ### scroll bottom
```
javascript:window.scrollTo(0, document.body.scrollHeight || document.documentElement.scrollHeight);
```
- ### search site
```
javascript:var regularExpression=/\/([^\s\/]+)/g;var match=regularExpression.exec(window.location);var searchString=match[1];window.location="http://www.google.com/search?q=site:"+searchString+encodeURIComponent(" ");
```
- ### search site ddg
```
javascript:var regularExpression=/\/([^\s\/]+)/g;var match=regularExpression.exec(window.location);var searchString=match[1];window.location="http://www.duckduckgo.com/?q=site:"+searchString+encodeURIComponent(" ");
```
- ### seletion + url
```
javascript:var stext="";var sdom="";stext=window.getSelection().toString();sdom=document.location;window.prompt("Copy to clipboard: Ctrl+C",stext+" \u2013 ( "+sdom+" )");stext=null;sdom=null;
```
- ### show links
```
javascript:var a='';for(var ln=0;ln<document.links.length;ln++){var lk=document.links[ln];a+=ln+': <a href=\''+lk+'\' title=\''+lk.text+'\'>'+lk+'</a><br>\n';}w=window.open('','Links','scrollbars,resizable,width=400,height=600');w.document.write(a);
```
- ### show passwords
```
javascript:(function(){var IN,F;IN=document.getElementsByTagName('input');for(var i=0;i<IN.length;i++){F=IN[i];if(F.type.toLowerCase()=='password'){try{F.type='text'}catch(r){var n,Fa;n=document.createElement('input');Fa=F.attributes;for(var ii=0;ii<Fa.length;ii++){var k,knn,knv;k=Fa[ii];knn=k.nodeName;knv=k.nodeValue;if(knn.toLowerCase()!='type'){if(knn!='height'&&knn!='width'&&!!knv)n[knn]=knv}};F.parentNode.replaceChild(n,F)}}}})()
```
- ### show title
```
javascript:var titletag=document.getElementsByTagName('title')[0].innerText;var tytul=document.getElementsByClassName('title');var ft=document.getElementsByClassName('barrier__heading-serif');if(tytul.length<=0){tytul='Title Class does not exist!';}else{tytul=document.getElementsByClassName('title')[0].innerText;}if(titletag.length<=0){titletag='There is no <title> tag on this page!';}else{titletag=document.getElementsByTagName('title')[0].innerText;}if(ft.length<=0){ft='';}else{ft='\nFT Title: '+document.getElementsByClassName('barrier__heading-serif')[0].innerHTML;}alert('<TITLE> '+titletag+'</TITLE>\nTitle class: '+tytul+ft);
```
- ### show site info
```
javascript:void(window.open('http://builtwith.com/?'+location.host));
```
- ### site search
```
javascript:var regularExpression=/((&|\?)q=)([^&]*)(?!.*&q=)/g;var match=regularExpression.exec(window.location);var searchString=match[3];var searchArray=searchString.split("+");var siteSearchTerm=searchArray.pop();var siteSearchTermArray=siteSearchTerm.split(".");if(siteSearchTermArray.length==1||siteSearchTermArray.pop().length>3){siteSearchTerm=siteSearchTerm+".com";}if(siteSearchTerm.indexOf("site")==-1){var siteSearchTerm="site:"+siteSearchTerm;}searchArray.push(siteSearchTerm);window.location="http://www.google.com/search?q="+searchArray.join("+");
```
- ### sort tables
```
javascript:function toArray(c){var a,k;a=new Array;for(k=0;k<c.length;++k)a[k]=c[k];return a;}function insAtTop(par,child){if(par.childNodes.length)par.insertBefore(child,par.childNodes[0]);else par.appendChild(child);}function countCols(tab){var nCols,i;nCols=0;for(i=0;i<tab.rows.length;++i)if(tab.rows[i].cells.length>nCols)nCols=tab.rows[i].cells.length;return nCols;}function makeHeaderLink(tableNo, colNo, ord){var link;link=document.createElement('a');link.href='javascript:sortTable('+tableNo+','+colNo+','+ord+');';link.appendChild(document.createTextNode((ord>0)?'↑':'↓ '));return link;}function makeHeader(tableNo,nCols){var header,headerCell,i;header=document.createElement('tr');for(i=0;i<nCols;++i){headerCell=document.createElement('td');headerCell.appendChild(makeHeaderLink(tableNo,i,1));headerCell.appendChild(document.createTextNode('/'));headerCell.appendChild(makeHeaderLink(tableNo,i,-1));header.appendChild(headerCell);}return header;}g_tables=toArray(document.getElementsByTagName('table'));if(!g_tables.length)alert("This page doesn't contain any tables.");(function(){var j,thead;for(j=0;j<g_tables.length;++j){thead=g_tables[j].createTHead();insAtTop(thead, makeHeader(j,countCols(g_tables[j])))}})();function compareRows(a,b){if(a.sortKey===b.sortKey)return 0;return (a.sortKey < b.sortKey) ? g_order : -g_order;}function sortTable(tableNo, colNo, ord){var table,rows,nR,bs,i,j,temp;g_order=ord;g_colNo=colNo;table=g_tables[tableNo];rows=new Array();nR=0;bs=table.tBodies;for(i=0; i<bs.length; ++i)for(j=0; j<bs[i].rows.length; ++j){rows[nR]=bs[i].rows[j];temp=rows[nR].cells[g_colNo];if(temp)rows[nR].sortKey=temp.innerHTML;else rows[nR].sortKey="";;++nR;}rows.sort(compareRows);for (i=0; i < rows.length; ++i)insAtTop(table.tBodies[0], rows[i]);}
```
