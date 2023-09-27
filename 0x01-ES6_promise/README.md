Project Title: ES6 Promises
Description
This project focuses on understanding and working with ES6 Promises in JavaScript. It covers various concepts such as Promises, then, resolve, catch methods, await, async functions, and error handling using try and catch.

Learning Objectives
Upon completion of this project, you will be able to:

Explain what Promises are, their purpose, and how to use them.
Utilize the then, resolve, and catch methods for working with Promises.
Understand and apply the await operator and create async functions.
Handle errors using try and catch.
Project Tasks
Task 0: Keep every promise you make and only make promises you can keep
Implement getResponseFromAPI function that returns a Promise.
Example usage:
javascript
Copy code
import getResponseFromAPI from "./0-promise.js";
const response = getResponseFromAPI();
console.log(response instanceof Promise); // Output: true
Task 1: Don't make a promise...if you know you can't keep it
Implement getFullResponseFromAPI(success) function that returns a Promise.
Example usage:
javascript
Copy code
import getFullResponseFromAPI from './1-promise';
console.log(getFullResponseFromAPI(true)); // Output: Promise { { status: 200, body: 'Success' } }
console.log(getFullResponseFromAPI(false)); // Output: Promise { <rejected> Error: The fake API is not working currently }
Task 2: Catch me if you can!
Implement handleResponseFromAPI(promise) function to handle resolved and rejected Promises.
Example usage:
javascript
Copy code
import handleResponseFromAPI from "./2-then";
const promise = Promise.resolve();
handleResponseFromAPI(promise); // Output: Got a response from the API
Task 3: Handle multiple successful promises
Import uploadPhoto and createUser functions from utils.js.
Implement handleProfileSignup() function to handle multiple promises and log results.
Example usage:
javascript
Copy code
import handleProfileSignup from "./3-all";
handleProfileSignup(); // Output: photo-profile-1 Guillaume Salva
Task 4: Simple promise
Implement signUpUser(firstName, lastName) function that returns a resolved Promise.
Example usage:
javascript
Copy code
import signUpUser from "./4-user-promise";
console.log(signUpUser("Bob", "Dylan")); // Output: Promise { { firstName: 'Bob', lastName: 'Dylan' } }
Task 5: Reject the promises
Write and export uploadPhoto(filename) function that returns a Promise rejecting with an Error.
Example usage:
javascript
Copy code
import uploadPhoto from './5-photo-reject';
console.log(uploadPhoto('guillaume.jpg')); // Output: Promise { <rejected> Error: guillaume.jpg cannot be processed }
Task 6: Handle multiple promises
Import signUpUser from 4-user-promise.js and uploadPhoto from 5-photo-reject.js.
Implement handleProfileSignup(firstName, lastName, fileName) function to handle multiple promises and return an array of results.
Task 7: Load balancer
Write and export loadBalancer(chinaDownload, USDownload) function that returns the value of the first resolved promise.
Task 8: Throw error / try catch
Write and export divideFunction(numerator, denominator) function that handles division by zero and throws an error.
Task 9: Throw an error
Write and export guardrail(mathFunction) function that appends results or errors to an array.
Task 10: Await / Async (Advanced)
Import uploadPhoto and createUser from utils.js.
Implement asyncUploadUser() async function that calls both functions and returns an object.
Requirements
All files executed on Ubuntu 18.04 LTS using NodeJS 12.11.x.
Allowed editors: vi, vim, emacs, Visual Studio Code.
All files should end with a new line.
A README.md file, at the root of the folder, is mandatory.
Code files should use the .js extension.
Code will be tested using Jest and the command npm run test.
Code will be verified against lint using ESLint.
All functions must be exported.
Setup
Install NodeJS 12.11.x:

bash
Copy code
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
nodejs -v # Should output v12.11.1
npm -v # Should output 6.11.3
Install Jest, Babel, and ESLint:

In your project directory, run:

bash
Copy code
npm install
Add the provided configuration files to your project directory:

package.json
babel.config.js
utils.js
.eslintrc.js
Make sure to run npm install after adding package.json.

Response Data Format
uploadPhoto returns a response with the format:

javascript
Copy code
{
  status: 200,
  body: 'photo-profile-1',
}
createUser returns a response with the format:

javascript
Copy code
{
  firstName: 'Guillaume',
  lastName: 'Salva',
}
