# Sparkle Security Mission 2: File Upload XSS

This mission demonstrates another type of cross-site scripting
vulnerability.

# Introduction

Agent Sparkle, the agents of Project PoopyPants have yet another kind
of XSS vulnerability in their web application.  This lets us use their
web application to post our messages to other agents.

# Our Payload

Our payload is an HTML file (the markup language that forms web pages)
that renders our message in browsers.  Cut and paste this into [file_upload_xss.html](https://raw.githubusercontent.com/terriko/sparklesecurity/master/file_upload_xss.html):
```
<html>
<head>
<style type="text/css">
    body {
      margin-top: 1.0em;
      background-color: #faf8f5;
      font-family: Comfortaa, Arial, FreeSans, san-serif;
      color: #000000;
    }
    section,header,footer{display:block}
    #container {
      margin: 0 auto;
      width: 800px;
    }
    
    h1 { font-size: 3.8em; color: #05070a; margin-bottom: 3px; font-family:monoton,helvetica,arial,sans-serif;position:relative}
    h1 span{position:absolute;right:0;top:10px}
    h1 a { text-decoration: none }
    h2 { font-size: 1.5em; color: #05070a; }
    h3 { text-align: center; color: #05070a; }
    a { color: #05070a; }
    .description { font-size: 1.2em; margin-bottom: 30px; margin-top: 30px; font-style: italic;}
    .download { float: right; }
    pre { background: #000; color: #fff; padding: 15px;}
    hr { border: 0; width: 80%; border-bottom: 1px solid #aaa}
    .footer { text-align:center; padding-top:30px; font-style: italic; }
    
/*
 * CSS animated rainbow dividers of awesome 
 * by Chris Heilmann @codepo8 and Lea Verou @leaverou 
**/
@-moz-keyframes charlieeee {
  from { background-position:top left; } 
  to {background-position:top right; }
}
@-webkit-keyframes charlieeee { 
  from { background-position:top left; }  
  to { background-position:top right; }  
}
@-o-keyframes charlieeee { 
  from { background-position:top left; }  
  to { background-position:top right; }  
}
@-ms-keyframes charlieeee { 
  from { background-position:top left; }  
  to { background-position:top right; }  
}
@-khtml-keyframes charlieeee { 
  from { background-position:top left; }  
  to { background-position:top right; }  
}
@keyframes charlieeee { 
  from { background-position:top left; }  
  to { background-position:top right; }  
}
.catchadream{
  background-image:-webkit-linear-gradient( left, red, orange, yellow, green,
                                          blue, indigo, violet, indigo, blue,
                                          green, yellow, orange, red );
  background-image:-moz-linear-gradient( left, red, orange, yellow, green,
                                         blue,indigo, violet, indigo, blue,
                                         green, yellow, orange,red );
  background-image:-o-linear-gradient( left, red, orange, yellow, green,
                                         blue,indigo, violet, indigo, blue,
                                         green, yellow, orange,red );
  background-image:-ms-linear-gradient( left, red, orange, yellow, green,
                                         blue,indigo, violet, indigo, blue,
                                         green, yellow, orange,red );
  background-image:-khtml-linear-gradient( left, red, orange, yellow, green,
                                         blue,indigo, violet, indigo, blue,
                                         green, yellow, orange,red );
  background-image:linear-gradient( left, red, orange, yellow, green,
                                         blue,indigo, violet, indigo, blue,
                                         green, yellow, orange,red );
  -moz-animation:charlieeee 2.5s forwards linear infinite;
  -webkit-animation:charlieeee 2.5s forwards linear infinite;
  -o-animation:charlieeee 2.5s forwards linear infinite;
  -khtml-animation:charlieeee 2.5s forwards linear infinite;
  -ms-animation:charlieeee 2.5s forwards linear infinite;
  -lynx-animation:charlieeee 2.5s forwards linear infinite;
  animation:charlieeee 2.5s forwards linear infinite;
  background-size:50% auto;
}
#tongue{position:cheek;}
/* ^ OMG! An ID! That kills performance! */

  </style>
</head>
<body>
<h1 class="catchadream">OMG RAINBOWS!!!<h1>
</body>
</html>
```

# The Vulnerability

Project PoopyPants's application allows users to upload files, which
it then hosts for users.  However, it sets the Content-Type header in
the HTTP response based on the file extension.  This tells browsers to
display as a web page if the file type is HTML, which allows us to
host our message.

# Post Your Message

1.  Open http://127.0.0.1:8008/###################/upload.gtl
 Remember to replace ################### with your magic number.
2.  Upload the file_upload_xss.html file created above
3.  Visit the url that it returns and see the message

# Going Further

This type of vulnerability is dangerous because the html file can
contain scripts that execute in the same context as the application.
So, javascript on this page can actually access anything in the
http://127.0.0.1:8008/ origin.  Anything a user can do while logged
in, your stored script can do.  Can you make a script payload that
logs the user out?
