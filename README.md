# Know-abouts-of-Yup-a-Schema-validation-library->
This is a reference documentation to use Yup a schema validation library 

Yup, a schema validation library for JavaScript. It is commonly used in JavaScript frameworks and libraries, such as React, to handle form validation.
It provides a simple API that makes it easy to define validation rules for your data. 
Yup also provides a number of built-in validation rules, such as required, email, min, max and number.

To define a schema in yup, you can use the object() method provided by yup. The object() method allows you to create a schema object that represents the structure and validation rules for your data object.
const schema = yup.object().shape({
  // Define your fields and their validation rules here
});

 
                                                       Here is a basic example of using Yup :

// Firstly Import Yup

import * as yup from "yup";



// Then Define a schema for a user

const userSchema = yup.object().shape({

  name: yup.string().required(),

  email: yup.string().email().required(),

  password: yup.string().required(),

});



// Validate a user object

const user = {

  name: "John Doe",

  email: "johndoe@example.com",

  password: "password123",

};



const errors = userSchema.validate(user);



// Check if there are any errors

if (errors.length) {

  // There are errors

  console.log(errors);

} else {

  // The user object is valid

  console.log("The user object is valid");

}



                                                                      Explanation:-

In this example, we first import Yup into our project. Then, we define a schema for a user object. The schema specifies that the user object must have a name, email, and password property. The name and email properties must be strings and the password property must be a string of at least 8 characters.

Next, we create a user object and pass it to the validate() method of the userSchema object. The validate() method returns an array of errors if the user object does not meet the validation criteria. If there are no errors, the validate() method returns an empty array.

Finally, we check if the array of errors is empty. If it is empty, we know that the user object is valid. Otherwise, we log the errors to the console.

