# Happy-Button
Click and Get Complimented!
<!doctype html>
<html>
 <head> 
  <title>Sandboxing 101</title>
   <script>
// CREATE SENTANCES INTO NUMBERS IN ORDER TO % THEM??
 //HOOK UP REMAINDER VARIABLE TO  THE FUNCTION feelGoodButton.
 //So....how about an app that displays good news throughout the day. You also can send good news to a friend that they can download to their phone to display throughout the day. 
   var counter = 0;

   var someGoodMessages = ["You are an awesome person!" , "Thanks for pressing this button! You are great!" , "Keep trying! You can do impossible things!"];


   		var feelGoodButtonMessages = ["Press me to hear some good news!" , "You need to feel good about yourself, press me!", "Do you want to know something good about yourself? Press me!"];

   function numberCounter(numberCounter) {
   	
   		var remainder = counter % someGoodMessages.length;

         var buttonRemainder = counter % feelGoodButtonMessages.length;

   		var currentMessage = someGoodMessages[remainder];
   		document.getElementById("someGoodMessages").innerHTML = currentMessage;

   		var buttonMessage = feelGoodButtonMessages[buttonRemainder];
   		numberCounter.innerHTML = buttonMessage;

   		console.log(counter , remainder , buttonRemainder );
         counter += 1;

   	}
   function addToGoodMessages(){

      var messageInputBox = document.getElementById("yourGoodNews");

      if(messageInputBox.value.trim() == ""){

         messageInputBox.placeholder = "You didn't add anything. Put in some good news!";

      }

      else{
         someGoodMessages.push(messageInputBox.value);
         messageInputBox.placeholder = "Hey! Add some good news!";
      }

      messageInputBox.value = null;
      

   }

   </script>
   <style>
   textarea{
      width: 250px;
      height: 100px;
   }
   </style>
 </head>
 <body>
 
 	<button onclick="numberCounter(this)">Hey...press here for something cool.</button>



 	<p>Good News: <a id="someGoodMessages"></a></p>

   <section id="hidden_note_number"></section>

      <p><textarea id="yourGoodNews" placeholder= "Hey! Add some good news!"></textarea></p>

   <button onclick="addToGoodMessages()">Add to the good news! :)</button>

 </body>
 </html>
