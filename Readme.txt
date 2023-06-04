Thanks for downloading this template!

Template Name: BizPage
Template URL: https://bootstrapmade.com/bizpage-bootstrap-business-template/
Author: BootstrapMade.com
License: https://bootstrapmade.com/license/


    thisForm.querySelector('.loading').classList.add('d-block');
    thisForm.querySelector('.error-message').classList.remove('d-block');
    thisForm.querySelector('.sent-message').classList.remove('d-block');

    thisForm.querySelector('.loading').classList.remove('d-block');




$(document).ready(function(){
    // click on button submit
    $("#submit").on('click', function(){
        // send ajax
        $.ajax({
            url: 'test.php', // url where to submit the request
            type : "POST", // type of action POST || GET
            dataType : 'json', // data type
            data : $("#form").serialize(), // post data || get data
            success : function(result) {
                // you can see the result from the console
                // tab of the developer tools
                console.log(result);
            },
            error: function(xhr, resp, text) {
                console.log(xhr, resp, text);
            }
        })
    });
});



var form = document.querySelector('form');
form.onsubmit = function(event){
    var formData = new FormData(form);
    
    fetch("https://unilorinwaterquality.com.ng/mail_post.php",
    {
       body: formData,
       method: "post"
    }).then();
    
    //Dont submit the form.
    return false; 
}


        {
            thisForm.querySelector('.loading').classList.remove('d-block');
            thisForm.querySelector('.sent-message').classList.add('d-block');
            thisForm.reset();  
      }



response => {
        if( response.ok ) {
            thisForm.querySelector('.loading').classList.remove('d-block');
            thisForm.querySelector('.sent-message').classList.add('d-block');
            thisForm.reset(); 
        } else {
          throw new Error(`${response.status} ${response.statusText} ${response.url}`); 
        }
      }