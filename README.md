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

