# escapebutton
This is a JavaScript escape button suitable for use by Domestic Abuse Shelters and others

Okay, since nobody ever explains to me how this sh!t works, here you go:

YOU PUT THIS IN THE BODY PORTION OF YOUR PAGE

   <div style="background-color: #FFF; color: #000; position: fixed; right: 0; bottom: 0; font-size: 3em;" onclick="Navigate()">ESCAPE</button></div>
   
THIS GOES IN THE HEAD

  <script type="text/javascript">
    function Navigate(){   
         window.location.replace('https://google.com');
        return false;
    }
   </script>
   
Together, they make a link that should align at the bottom-right portion of the page.  Click it, it replaces the CURRENT history item with whatever's in window.location.replace.

Yes, this is very simple, BUT I SAW SOMEONE CHARGING $25 FOR THIS.  That motherf!cker.

IF YOU WANT TO PROTECT AN ENTIRE WEBSITE, MAKE THE INDEX.HTML LOOK SOMETHING LIKE THIS


<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd">
<html>
	<head><title>Any Title you Want</title>

</head>
	<frameset rows="*,0" border="0" frameborder="0"> 
		<frame id="main" src="YOURREALMAINPAGE.html" />
		<frame id="hidden" src="about:blank"/>
	</frameset><noframes></noframes>

</div>
</html>



Put the stuff above all this into YOURREALMAINPAGE.html and it should work.  You don't NEED to put the thing in frames (it does not work well on mobile) but if you need to protect AN ENTIRE WEBSITE instead of just one page, this'll do it.

gl hf dd ka
