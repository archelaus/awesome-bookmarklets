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
javascript:(function()%7Bfunction%20getParameterByName(e%2Ct)%7Be%3De.replace(%2F%5B%5C%5B%5D%2F%2C%22%5C%5C%5B%22).replace(%2F%5B%5C%5D%5D%2F%2C%22%5C%5C%5D%22)%3Bvar%20n%3Dnew%20RegExp(%22%5B%5C%5C%3F%26%5D%22%2Be%2B%22%3D(%5B%5E%26%23%5D*)%22)%2Cr%3Dn.exec(t%3D%3Dtrue%3Flocation.hash.replace(%22%23%22%2C%22%3F%22)%3Alocation.search)%3Bif(r%3D%3Dnull%26%26t%3D%3Dfalse)%7Breturn%20getParameterByName(e%2Ctrue)%7Delse%7Breturn%20r%3D%3Dnull%3F%22%22%3AdecodeURIComponent(r%5B1%5D.replace(%2F%5C%2B%2Fg%2C%22%20%22))%7D%7Dstr%3D%22%3Cstyle%20type%3D%27text%2Fcss%27%3Ebody%7Bcolor%3A%23000%3Bbackground-color%3A%23fff%3Bmargin%3A0%3Bpadding%3A0%3Bfont-family%3Aarial%2Chelvetica%2Csans-serif%3Bfont-size%3A82%25%7D*%7Bfont-weight%3A400%3Bcolor%3A%23000%7Dh3%2Ch4%2Ch5%2Ch6%7Bmargin%3A0%200%2015px%3Bpadding%3A0%7D%23rt%7Bfont-size%3A12px%3Bwidth%3A500px%7Dtable%2Ctd%2Cth%2Ctr%7Bfont-size%3A1em%3Boverflow%3Ahidden%3Btext-overflow%3Aellipsis%3Bword-wrap%3Abreak-word%7Dtextarea%7Bwidth%3A100%25%7Dth%7Bbackground-color%3A%23eee%3Bcolor%3A%23000%3Bfont-weight%3A700%7Dtd%20a%7Bwidth%3A446px%3Bdisplay%3Ablock%7D.id%7Bbackground%3A%23eee%3Bcolor%3A%23000%3Btext-align%3Acenter%7D.g%7Bfont-family%3Aarial%2Csans-serif%3Bcolor%3A%23000%3Bmargin%3A1em%200%3Bfont-size%3A122%25%7D.g%20h2%7Bfont-family%3Aarial%2Csans-serif%3Bmargin%3A0%7D.r%7Bdisplay%3Ainline%3Bfont-weight%3A400%3Bmargin%3A10%7D.j%7Bwidth%3A34em%7D.std%7Bfont-size%3A82%25%7D.a%7Bcolor%3Agreen%7D.fl%7Bcolor%3A%2377c%7D.bl%7Bdisplay%3Ainline%7Da%7Bcolor%3A%2300c%7Da%3Avisited%7Bcolor%3A%23551a8b%7Da%3Aactive%7Bcolor%3Ared%7D.twitter-share-button%7Bmargin-bottom%3A-5px%7Dp.b%7Bline-height%3A22px%3Btext-align%3Acenter%7D%3C%2Fstyle%3E%5Cn%22%3Banchors%3Ddocument.getElementsByTagName(%22a%22)%3Bvar%20all%3D%5B%5D%3Bvar%20keyword%3DgetParameterByName(%22q%22%2Cfalse)%3Bstr%2B%3D%22%3Ctitle%3EGoogle%20SERP%20Scraper%20Bookmarklet%3C%2Ftitle%3E%22%3Bstr%2B%3D%22%3Cdiv%20style%3D%27width%3A%20900px%3B%20margin%3A%200%20auto%3B%27%3E%22%3Bstr%2B%3D%22%3Ch1%20style%3D%27margin%3A%201em%200em%200em%200em%3B%20text-align%3A%20center%3B%27%3EGoogle%20SERP%20Scraper%20Bookmarklet%3C%2Fh1%3E%22%3Bstr%2B%3D%22%3Ch2%20style%3D%27text-align%3A%20center%3B%27%3EKeyword%20-%20%22%2Bkeyword%2B%22%3C%2Fh2%3E%22%3Bstr%2B%3D%22%3Ctable%20width%3D%27100%25%27%3E%22%3Bstr%2B%3D%22%3Ctr%3E%3Cth%20width%3D%275%25%27%3EResult%3C%2Fth%3E%3Cth%20width%3D%2750%25%27%3ELink%3C%2Fth%3E%3Cth%20width%3D%2745%25%27%3EAnchor%20Text%3C%2Fth%3E%3C%2Ftr%3E%5Cn%22%3Bvar%20tweetText%3D%27%3Cp%20class%3D%22b%22%3EIf%20you%20use%20and%20like%20this%2C%20please%20%3Ca%20href%3D%22https%3A%2F%2Ftwitter.com%2Fshare%22%20class%3D%22twitter-share-button%22%20data-count%3D%22none%22%20data-lang%3D%22en%22%20data-url%3D%22http%3A%2F%2Fcognitiveseo.com%2Fblog%2F5714%2F69-amazing-seo-bookmarklets-to-supercharge-your-internet-marketing%2F%22%20data-text%3D%22%2F*Google%20SERP%20Scraper*%2F%20Bookmarklet%20%2B%2068%20Other%20Uber%20Amazing%20Bookmarklets%22%3ETweet%3C%2Fa%3E%20about%20it%20and%20help%20us%20spread%20the%20word.%3Cbr%20%2F%3E%20Happy%20SCRAPing%20and%20thanks%20for%20sharing!%3Cbr%20%2F%3E%20Coded%20by%20%3Ca%20href%3D%22http%3A%2F%2Fcognitiveseo.com%2F%22%20target%3D%22_blank%22%3EcognitiveSEO%3C%2Fa%3E.%3C%2Fp%3E%27%3Bvar%20tweetScript%3D%27%3Cscript%3E!function(d%2Cs%2Cid)%7Bvar%20js%2Cfjs%3Dd.getElementsByTagName(s)%5B0%5D%3Bif(!d.getElementById(id))%7Bjs%3Dd.createElement(s)%3Bjs.id%3Did%3Bjs.src%3D%22https%3A%2F%2Fplatform.twitter.com%2Fwidgets.js%22%3Bfjs.parentNode.insertBefore(js%2Cfjs)%3B%7D%7D(document%2C%22script%22%2C%22twitter-wjs%22)%3B%3C%2Fscript%3E%27%3Bvar%20k%3D0%3Bvar%20listing%3D%22%22%3Bvar%20links%3D%22%22%3Bvar%20anchorTexts%3D%22%22%3Bvar%20linksAnchors%3D%22%22%3Bfor(i%3D0%3Bi%3Canchors.length%3Bi%2B%2B)%7Bvar%20anchorText%3Danchors%5Bi%5D.textContent%3Bvar%20anchorLink%3Danchors%5Bi%5D.href%3Bvar%20linkAnchor%3D%22%22%3Bif(anchorLink.match(%2F%5E((%3F!google%5C.%7Ccache%7C%5C.yahoo%5C.%7Cyoutube%5C.com%5C%2Fresults%7Cjavascript%3A%7B%7D%7Cjavascript%3Avoid%7Cjavascript%3A%5C%3B%7Capi%5C.technorati%5C.com%7Cbotw%5C.org%5C%2Fsearch%7Cdel%5C.icio%5C.us%5C%2Furl%5C%2Fcheck%7Cdigg%5C.com%5C%2Fsearch%7Csearch%5C.twitter%5C.com%5C%2Fsearch%7Csearch%5C.yahoo%5C.com%5C%2Fsearch%7Csiteanalytics%5C.compete%5C.com%7Ctools%5C.seobook%5C.com%5C%2Fgeneral%5C%2Fkeyword%5C%2Fsuggestions%7Cweb%5C.archive%5C.org%5C%2Fweb%5C%2F%7Cwhois%5C.domaintools%5C.com%7Cwww%5C.alexa%5C.com%5C%2Fdata%5C%2Fdetails%5C%2Fmain%7Cwww%5C.bloglines%5C.com%5C%2Fsearch%7Cwww%5C.majesticseo%5C.com%5C%2Fsearch%5C.php%7Cwww%5C.semrush%5C.com%5C%2Finfo%5C%2F%7Cwww%5C.semrush%5C.com%5C%2Fsearch%5C.php%7Cwww%5C.stumbleupon%5C.com%5C%2Furl%7Cwikipedia.org%5C%2Fwiki%5C%2FSpecial%3ASearch).)*%24%2Fi)%26%26anchorLink!%3D%22%22%26%26all.indexOf(anchorLink)%3D%3D-1%26%26anchorText!%3D%22%22%26%26anchors%5Bi%5D.className!%3D%22gb_b%22)%7Ball.push(anchorLink)%3Blisting%2B%3DanchorLink%2B%22%5Cn%22%3BanchorTexts%2B%3DanchorText%2B%22
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
- ### stop editing
```
javascript:document.body.contentEditable='false';document.designMode='off';void 0;
```
- ### summate
```
javascript:void(window.open("https://summate.it/"+location.href, "_self"));
```
- ### switch hn
```
javascript:(function(){var a=window.location.href;a.match(/news\.ycombinator\.com/i)?(b=a.match(/item\?id=(\d+)/i)[1],window.location.href="https://hackernewz.com/item/"+b):a.match(/hackernewz\.com/i)&&(b=a.match(/item\/(\d+)/i)[1],window.location.href="https://news.ycombinator.com/item?id="+b);})();
```
- ### texed
```
data:text/html,<title>texed</title><body style=margin:0><textarea autofocus spellcheck=false style=width:100vw;height:100vh;resize:none;border:0;padding:6pt;font-family:monospace;font-size:large;background-color:rgb(22,22,22);color:lightyellow>
```
- ### text analytices
```
javascript:!function(){function e(e){return e&&""!==e&&(e=e.trim(),e=e.replace(/%5Cs+/gi," "),e=e.replace(/%5B%5Ea-zA-Z0-9%20%5D/gi,""),e.split(" ")):0}var t=function(t){var n=e(t)||[],r=t.length;if(0==n.length)return null;var i=0;n.forEach(function(e){i+=e.length}),i/=n.length;var o=n.reduce(function(e,t){return e.length<=t.length?e:t}),a=n.reduce(function(e,t){return e.length>=t.length?e:t});return{wordCount:n.length,charCount:r,minWord:o,maxWord:a,avgLen:i}},n=document.createElement("div");n.setAttribute("style","color:black;    position:fixed;    left:5%;    top:5%;    width:150px;    height:auto;    font-size:14px;    z-index:10000;    background:white;    border-radius:0px;    border:1px solid grey;    padding:5px 2px 5px 4px;"),n.setAttribute("id","analyticsbox");var r="";window.getSelection&&(r=window.getSelection().toString());var i=t(r),o=document.createElement("div");o.setAttribute("style","margin:5px;    font-family:serif;    line-height:1.2em;    font-size:16px;"),null==i?o.innerHTML="No text selected.<br/>Select some text and click the bookmark to run text analysis.":(o.innerHTML="Words: "+i.wordCount+"<br/>",o.innerHTML+="Chars: "+i.charCount+"<br/><br/>",o.innerHTML+="<span>Advanced Lengths</span><br/><br/>",o.innerHTML+="Avg Word: "+i.avgLen+"<br/>",o.innerHTML+="Min Word: "+i.minWord.length+"<br/>",o.innerHTML+="Max Word: "+i.maxWord.length+"<br/>"),n.appendChild(o);var a=document.createElement("div");a.setAttribute("style","    color:black;    position:absolute;    right:6px;    top:5px;    width:auto;    font-size:14px;    text-align:right;    font-family:Arial, sans-serif;    cursor:pointer;"),a.appendChild(document.createTextNode("X")),a.setAttribute("id","textAnalyticsClose"),n.appendChild(a),a.addEventListener("click",function(){n.style.display="none"},!1),document.body.appendChild(n)}();
```
- ### unddit
```
javascript:window.open(location.href.replace(/:\/\/([\w-]+\.)?(reddit\.com\/r|reveddit\.com\/v)\//i, "://www.unddit.com/r/"), "_blank")
```
- ### urban dictionary
```
javascript:(function(){q=document.getSelection();if(!q){void(q=prompt('Slang to look up:',''))};if(q)location.href='http://www.urbandictionary.com/define.php?term='+escape(q)})()
```
- ### vxtwitter
```
javascript:(function(){function%20copyToClipboard(t){if(navigator.clipboard&&navigator.clipboard.writeText)return%20navigator.clipboard.writeText(t);else%20if(window.clipboardData&&window.clipboardData.setData)return%20clipboardData.setData("Text",t);else%20if(document.queryCommandSupported&&document.queryCommandSupported("copy")){var%20e=document.createElement("textarea");return%20e.textContent=t,e.style.position="fixed",document.body.appendChild(e),e.select(),document.execCommand("copy"),document.body.removeChild(e),!0}else%20return!1}var%20t=window.location.href;if(t.includes("twitter.com")||t.includes("nitter.nl")){t=t.replace("twitter.com","vxtwitter.com").replace("nitter.nl","vxtwitter.com"),copyToClipboard(t)}else%20alert("This%20bookmarklet%20only%20works%20on%20Twitter%20or%20Nitter%20pages.")})();
```
- ### wayback cache
```
javascript:window.location.href='https://web.archive.org/web/'+window.location.href.replace(/^https?:\/\//i,'');
```
- ### wayack
```
javascript:void(window.open('https://web.archive.org/web/*/'+escape(location.href.replace(/^https?:\/\//,'').replace(/\/$/,''))));
```
- ### web2pdf
```
javascript:void(window.open('https://www.web2pdfconvert.com#' + location.href))
```
- ### web qr code
```
javascript:(function(){var url=('http://chart.apis.google.com/chart?cht=qr&chs=300x300&chl=' + encodeURIComponent(location.href));w = open(url, 'w', 'location=no,status=yes,menubar=no,scrollbars=no,resizable=yes,width=500,height=500,modal=yes,dependent=yes');if (w) { setTimeout('w.focus()', 1000) } else { location = url } })();
```
- ### web stack
```
javascript:(function(){var d=document,e=d.getElementById('wappalyzer-container');if(e!==null){d.body.removeChild(e);}var u='https://www.wappalyzer.com/',t=new Date().getTime(),c=d.createElement('div'),p=d.createElement('div'),l=d.createElement('link'),s=d.createElement('script');c.setAttribute('id','wappalyzer-container');l.setAttribute('rel','stylesheet');l.setAttribute('href',u+'css/bookmarklet.css');d.head.appendChild(l);p.setAttribute('id','wappalyzer-pending');p.setAttribute('style','background-image:url('+u+'images/spinner.gif)!important');c.appendChild(p);s.setAttribute('src',u+'bookmarklet/wappalyzer.js');s.onload=function(){window.wappalyzer=new Wappalyzer();s=d.createElement('script');s.setAttribute('src',u+'bookmarklet/apps.js');s.onload=function(){s=d.createElement('script');s.setAttribute('src',u+'bookmarklet/driver.js');c.appendChild(s);};c.appendChild(s);};c.appendChild(s);d.body.appendChild(c);})();
```
- ### who.is
```
javascript:(function(){window.open("http://who.is/whois/" + document.domain)})();
```
- ### wikipedia
```
javascript:s=document.getSelection();for(i=0;i<frames.length;i++){if(s)break;s=frames[i].document.getSelection();}if(!s)void(s=prompt('Enter search terms for Wikipedia',''));wikiw=open('http://en.wikipedia.org/'+(s?'w/wiki.phtml?search='+escape(s):''));wikiw.focus();
```
- ### youtube rss feed
```
javascript:(function(){var url=(document.querySelector('link[type="application/rss+xml"]')||'').href;if(url!==undefined){return location.href=url;}try{var channelId=ytplayer.config.args.ucid;location.href='https://www.youtube.com/feeds/videos.xml?channel_id=' + channelId;}catch(TypeError){console.error('YouTube RSS feed bookmarklet: Could not find a channel RSS feed');}})();
```
- ### youtube shorten url
```
javascript:void(window.open('https://y2u.be/create.php?URL=' + location.href, '_self'));
```
- ### youtube thumbnail
```
javascript:(()=>{window.open(`https://img.youtube.com/vi/${new URLSearchParams(window.location.search).get("v")}/maxresdefault.jpg`);})();
```
- ### youtube download
```
javascript:void(open('https://qdownloader.net/download?video=' + encodeURIComponent(document.location)));
```
