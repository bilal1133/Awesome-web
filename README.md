# Awesome-web

* ## Native JS

  * ### Speak any Text Natively in Browser

    ```
     var u = new SpeechSynthesisUtterance();
     u.text = 'Web Speech API کا SpeechSynthesisUtterance انٹرفیس تقریر کی درخواست کی نمائندگی کرتا ہے۔ اس میں وہ مواد ہوتا ہے جو اسپیچ سروس کو پڑھنا چاہیے اور اسے پڑھنے کے طریقے کے بارے میں معلومات (جیسے زبان، پچ اور حجم۔)';
      u.lang = 'ur';
      u.rate = 1;
      u.onend = function(event) { alert('Finished in ' + event.elapsedTime + ' seconds.'); }
      speechSynthesis.speak(u);

      ```


  * ### Convert Audio to Text runtime in Browser

      ```
      const speechRecognition =
      window.speechRecognition || window.webkitSpeechRecognition;
    const recognition = new speechRecognition();
    SpeechRecognition.continuous = true;
    recognition.interimResults = true;
    recognition.lang = "en";
    recognition.onstart = function () {
      console.log("you can speek now");
    };
    speechRecognition.start()

    recognition.onresult = function (event) {
      var text = event.results[0][0].transcript;
      console.log(text);
      document.getElementById("result").innerHTML = text;
    };

      ```
   * ### Detect if a browser window is not currently active
      ```
      document.addEventListener( 'visibilitychange' , function() {
           if (document.hidden) {
               document.title = 'bye'
           } else {
               document.title = 'well back'
           }
       }, false );
      ```
