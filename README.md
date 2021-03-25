# Javascript-form-validation-and-prototype
Why JavaScript Form Validation?
Form need validation to prevent our web forms by malicious users. If your form doesn’t have proper validation, that might be one of the main causes of security vulnerabilities. Improper validations expose your website or application attacks such as SQL injections, header injections, cross-site scripting.

 

SQL Injection may lead to corrupt your backend database.

 

Header Injection can be used to send email spam from your web server.

 

Cross-site scripting may allow an attacker to send any data to your site.

 

While creating a form, validation of form data is based on the data type you specify for each field and for each data type only a specific set of characters are allowed.

 

For each field, it is important that form developers have to choose the correct data type.

 

[Read: Javascript String Methods | Properties | Objects]

 

Form validation examples:
In the following example, we are going to validate the name and password. Name cannot be empty and the password length should not less than 8.

 

<!DOCTYPE html>

<html>

<head>

   <meta charset='utf-8'>

   <meta http-equiv='X-UA-Compatible' content='IE=edge'>

   <title>Form Validation</title>

   <meta name='viewport' content='width=device-width, initial-scale=1'>

</head>

<script>

   function formValidation() {

       var name = document.RegForm.Name.value;  

       var password = document.RegForm.Password.value;  

       console.log(name);

       console.log(password);

       if (name == null || name == ""){  

           alert("Name can't be blank");  

           return false;  

       }

       if(password.length < 8){  

           alert("Password must be at least 8 characters long.");  

           return false;

       }

   }

</script>

<body>

   <form name="RegForm" action="" onsubmit="return formValidation()" method="post">  

       <p> Name: <input type="text" size="30" name="Name" > </p><br>        

       <p> Password: <input type="password" size="30" name="Password"> </p><br>

       <p><input type="submit" value="send" name="Submit"> </p>          

   </form>

</body>

</html>
 

[Read: Arrays in Javascript: Declaration | Properties | Array methods]

Retype password validation
In this example, we will check the first password and the second password is matched or not.

 

<script>

   function formValidation() {

       var passwordOne = document.RegForm.password1.value;  

       var passwordTwo = document.RegForm.password2.value;  

       if(passwordOne == passwordTwo){  

           return true;  

       }

       else{

       alert("password must be same!");  

           return false;  

       }

   }

</script>

<body>

   <form name="RegForm" action="" onsubmit="return formValidation()" method="post">  

       Password:<input type="password" name="password1" /><br/>  

       Re-enter Password:<input type="password" name="password2"/><br/>  

       <p><input type="submit" value="send" name="Submit"> </p>          

   </form>

</body>

</html>
[Read: Hapi file upload download]

Number validation:
Let’s validate the text field for numeric value only by using isNaN() function.

 

<script>

   function formValidation() {

       var num = document.RegForm.number.value;  

       if (isNaN(num)){  

           document.getElementById("numloc").innerHTML="Enter Numeric value only";  

           return false;

       }else{

           return true;  

       }

   }

</script>

<body>

   <form name="RegForm" action="" onsubmit="return formValidation()" method="post">  

       Number: <input type="text" name="number">

           <span id="numloc"></span><br/>  

       <input type="submit" value="submit">  

   </form>

</body>

</html>
Email validation:
To validate email in javascript, there are many criteria that need to be followed to validate the email is such as, email should contain @ and. characters, there must be at least one character before and after @ character, there must be at least two characters after .(dot).

 

<script>

   function formValidation() {

       var x = document.myform.email.value;  

       var atposition = x.indexOf("@");  

       var dotposition = x.lastIndexOf(".");  

       if (atposition<1 || dotposition<atposition+2 || dotposition+2>=x.length){  

           alert("Please enter a valid email address \n atpostion:"+atposition+"\n dotposition:"+dotposition);  

           return false;  

       }

   }

</script>

<body>

   <form name="RegForm" action="" onsubmit="return formValidation()" method="post">  

       Email: <input type="text" name="email"><br/>  

       <input type="submit" value="submit">  

   </form>

</body>
 

Javascript Prototype:

when a function is created in javascript then javascript engine adds a prototype property to the function and this prototype property is an object called a prototype object, which has a constructor prototype by default. Constructor property points back to the function and we can access the function’s prototype property using the syntax functionName.prototype.

 

Eg:

 

function Person(first, last, age, email) {

 this.firstName = first;

 this.lastName = last;

 this.age = age;

 this.email = email@domain.com;

}

var playerOne = new Person("MS", "Dhoni", 38, "dhoni@domain.com");

var playerTwo = new Person("Sachin", "Tendulkar", 46, "sachin.tendulkar@gmail.com");
 

You can not add a new property to an existing object constructor like following.

 

Eg:

 

Person.nationality = "India";
 

To add a new property to a constructor, you must add it to the constructor function like following.

 

Eg:

 

function Person(first, last, age, email) {

 this.firstName = first;

 this.lastName = last;

 this.age = age;

 this.email = email@domain.com;

 this.nationality = "India";

}
 

Prototype Inheritance:

All JavaScript objects inherit properties and methods from a prototype like date objects inherit from Date.prototype, Array objects inherit from Array.prototype and Person objects inherit from Person.prototype

 

Using the prototype Property

 

The JavaScript prototype property allows you to add new properties to object constructors as following.

 

Eg:

function Person(first, last, age, email) {

 this.firstName = first;

 this.lastName = last;

 this.age = age;

 this.email = email@domain.com;

}


Person.prototype.nationality = "India";
 

The JavaScript prototype property also allows you to add new methods to objects constructors as following

 

Eg:

function Person(first, last, age, email) {

 this.firstName = first;

 this.lastName = last;

 this.age = age;

 this.email = email@domain.com;

}

Person.prototype.name = function() {

 return this.firstName + " " + this.lastName;

};
 

[Read: Javascript: Closure with simple examples!]

 

If you’ve any doubts, please let us know through comment!!

Follow Us on Facebook | Twitter | LinkedIn.

Be it a software developer, programmer, coder, or a consultant, CronJ has it all. CronJ has been a trustworthy company for startups, small companies, and large enterprises. Hire the web of experienced ReactJS Development Services for your esteemed project today.

<a href="https://www.cronj.com/reactjs-development-company.html" rel="nofollow">ReactJS Development Services</a>


Let CronJ assist you..!

Thank you !!!
