# Registration-Form-Validation

<!DOCTYPE html>
<html>
  <head><title>Registration Form Validation</title></head>
  <body bgcolor="#E4F0F8">
    <script type="text/javascript">
      function formvalidator()
        {
          var firstname=document.getElementById('fristname');
          var lastname=document.getElementById('lastname');
          var email=document.getElementById('email');
          var pass=document.getElementById('pass');
          var addr=document.getElementById('addr');
          var mobileno=document.getElementById('mobileno');
          if(notEmpty(firstname,"first name can not be empty"))){
            if(isAlphabet(fristname,"Please enter only letters for your Frist name"))
            {
              if(lengthRestriction(fristname,6)){
                if(isAlphabet(lastname,"Please enter only letters for your Lastname")){
                  if(emailValidator(email,"Please enter a vaild email address")){
                    if(lengthRestriction(pass,,6)){
                      if(isAlphabet(pass,"PLease enter Numbers an dLetters only for password")){
                        if(notEmpty(addr,"please enter the address")){
                          if(isnumeric(mobileno,"please enter a vaild mobileno")){
                            if(lengthRegstriction(mobileno,10,10)){
                              return true;
                            }
                          }
                        }
                      }
                    }
                  }
                }
              }
            }
          }
          return false;
        }
      function notEmpty(elem,helperMsg){
        if(elem.value.length==0){
          alert(helperMsg);
          elem.focus();
          return false;
        }
        return true;
      }
      function isNumeric(elem,helperMsg){
        var numericExpression=/^[0-9]+$/;
        if(elem.value.match(numericExpression)){
          return true;
        }
        else{
          alert(helperMsg);
          elem.focus();
          return false;
        }
      }
      function isAplhabet(elem,helperMsg){
        var alphaExp=/^[a-zA-Z]+$/;
        if(elem.value.match(alphaExp)){
          return true;
        }
         else{
          alert(helperMsg);
          elem.focus();
          return false;
      }
        function isAplhanumeric(elem,helperMsg){
        var alphaExp=/^[0-9a-zA-Z]+$/;
        if(elem.value.match(alphaExp)){
          return true;
        }
         else{
          alert(helperMsg);
          elem.focus();
          return false;
      }
          function lengthRestriction(elem,min){
            var uInput=elem.value;
            if(uInput.length>=min){
              return true;
            }
            else{
              alert("Please enter minimum"+min+"characters");
              elem.focus();
              return flase;
            }
          }
        }
      }
    
