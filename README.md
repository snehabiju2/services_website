# services_website
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
const firebaseConfig = {
  apiKey: "AIzaSyBMODp6u_7DuU1kh1XDKkRTk2RbGR_aXg0",
  authDomain: "project-7ab29.firebaseapp.com",
  projectId: "project-7ab29",
  storageBucket: "project-7ab29.appspot.com",
  messagingSenderId: "225264127586",
  appId: "1:225264127586:web:6d8d9d568118a383460b3b"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);

function signIn()
{
  var email = document.getElementById("email").value;
  var password = document.getElementById("password").value;

  firebase.auth().signInWithEmailAndPassword(email, password)
    .then(function(userCredential) {
      // Sign-in is successful
      var user = userCredential.user;
      console.log("Signed in successfully: " + user.email);
      // Proceed to the next page or perform other actions
    })
    .catch(function(error) {
      // Sign-in failed
      var errorCode = error.code;
      var errorMessage = error.message;
      console.log("Sign-in failed. Error code: " + errorCode + ", Error message: " + errorMessage);
    });
}


const loginForm = document.getElementById('loginForm');
loginForm.addEventListener('submit', (e) => {
  e.preventDefault(); // Prevent form submission

  const email = document.getElementById('email').value;
  const password = document.getElementById('password').value;

  // Sign in user using Firebase Authentication
  firebase.auth().signInWithEmailAndPassword(email, password)
    .then((userCredential) => {
      // Login successful, redirect to home page
      window.location.href = 'home.html';
    })
    .catch((error) => {
      // Handle login error
      console.error(error);
    });
});


<a href="home.html">Go to Home</a>
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";

// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyAqLdD_QDjhN9g3HLA_PPDtK-8-gZoOe2k",
  authDomain: "services-project-d9012.firebaseapp.com",
  projectId: "services-project-d9012",
  storageBucket: "services-project-d9012.appspot.com",
  messagingSenderId: "801261924275",
  appId: "1:801261924275:web:2add6cf0adb9d12541a5c6",
  measurementId: "G-B1Q8NLNHJG"
};

// Initialize Firebase


// Initialize Firebase
//const db = getFirestore()
const app = initializeApp(firebaseConfig);
//const analytics = getAnalytics(app);


function registerForm() {
   // document.getElementById("formElement").addEventListener("submit", function() {
        // Perform necessary actions
      
        // Return false to prevent the default behavior
    //    return false;
     // });
  
    // Get user input from the sign-up form
    const email = document.getElementById("email").value;
    const password = document.getElementById("psw").value;
    const password2 = document.getElementById("psw_repeat").value;
    if(password==password2){
    // Create a new user with email and password
    var auth = firebase.auth();
    auth.createUserWithEmailAndPassword(email, password)
    .then((userCredential) => {
      // User sign-up successful
      const user = userCredential.user;
      console.log("User signed up:", user);
      // Additional actions after successful sign-up
    })
    .catch((error) => {
      // Handle sign-up errors
      const errorCode = error.code;
      const errorMessage = error.message;
      console.error("Sign-up error:", errorCode, errorMessage);
    });;
}
else {
    // Passwords do not match
    console.error("Passwords do not match");
    // Display an error message to the user or perform any other necessary action
  }
  }

  
var registerButton = document.getElementById('registerButton');

// Add click event listener to the sign-in button
registerButton.addEventListener('click', function() {
  // Simulating successful sign-in
  var isSignedIn = true;

  if (isSignedIn) {
    // Redirect to the home page
    window.location.href = 'home.html';
  }
});


import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
  apiKey: "AIzaSyAqLdD_QDjhN9g3HLA_PPDtK-8-gZoOe2k",
  authDomain: "services-project-d9012.firebaseapp.com",
  projectId: "services-project-d9012",
  storageBucket: "services-project-d9012.appspot.com",
  messagingSenderId: "801261924275",
  appId: "1:801261924275:web:2add6cf0adb9d12541a5c6",
  measurementId: "G-B1Q8NLNHJG"
};
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);

const loginForm = document.getElementById('loginForm');
loginForm.addEventListener('submit', (e) => {
  e.preventDefault(); // Prevent form submission

  const email = document.getElementById('email').value;
  const password = document.getElementById('password').value;

  // Sign in user using Firebase Authentication
  firebase.auth().signInWithEmailAndPassword(email, password)
    .then((userCredential) => {
      // Login successful, redirect to home page
      window.location.href = 'home.html';
    })
    .catch((error) => {
      // Handle login error
      console.error(error);
    });
});
function signIn()
{
  var email = document.getElementById("email").value;
  var password = document.getElementById("password").value;

  firebase.auth().signInWithEmailAndPassword(email, password)
    .then(function(userCredential) {
      // Sign-in is successful
      var user = userCredential.user;
      console.log("Signed in successfully: " + user.email);
      // Proceed to the next page or perform other actions
    })
    .catch(function(error) {
      // Sign-in failed
      var errorCode = error.code;
      var errorMessage = error.message;
      console.log("Sign-in failed. Error code: " + errorCode + ", Error message: " + errorMessage);
    });
}

