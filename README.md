# my-web-projects
My Front-End Project using HTML, CSS, JS
<html>
  <head>
    
    
  </head>
    <body>
      <!--Container tags-->
      <!--Tags like div, span, header, footer, main-->
      <!-- Only used in grouping other HTML tags, they dont have their job-->
      <!-- In-Line and block level elements-->
      <!-- Class names and ID names-->
      
      <header><!--Container tag-->
              
      <h1>Ananya</h1>
      <h4 class="one-line">Electronics Student</h4>   
      <!-- 20 headings after this-->
      </header>
      <nav><!--Container tag-->
      <ul>
          <li><a href="#education">Education</a></li>
          <li><a href="#certifications">Certifications</a></li>
          <li><a href="#hobbies">Hobbies</a></li>
          <li><a href="#contact-me">Contact Me</a></li>
          <li><a href="#admin-login" onClick= "showAdminLogin()">Admin Login</a></li>
      </ul>
      </nav>
      <button id="switch-theme">Toggle Theme</button>
      
      <main><!--Container tag-->
        <!--
        I was very bright student in <div> school</div> but covid made me dump 
        in <span> college</span> and hence all gen Z tend to be dump :p-->
        <section class="section-style" id="education"><!--Container tag--> 
        <h2 class="cls1"> Education</h2>
          <div><!--Container tag-->
        <h3> B.tech </h3>
        <p>2022-2026</p>
          </div>
          <div>
        <h3> High School </h3>
        <p>2019</p>
          </div>
         </section>
        
         <section class="section-style" id="certifications"><!--Container tag--> 
        <h2>Certifications</h2>
          <div><!--Container tag-->
        <h3> Introduction to modern AI </h3>
        <p>Cisco Networking Academy</p>
          </div>
          <div>
        <h3> Introduction to Python </h3>
        <p>Infosys Springboard</p>
          </div>       
        </section>
        
         <section class="section-style" id="hobbies"><!--Container tag--> 
        <h2>Hobbies</h2>
          <div><!--Container tag-->
        <h3> Singing</h3>
        <p>All songs like Devotional, Love, Folk</p>
          </div>
          <div>
        <h3> Photography  </h3>
        <p> Love to click Photos of Leaves or Flowers or any other places </p>
          </div>       
        </section>
        
         <section class="section-style" id="contact-me"><!--Container tag--> 
        <h2>Contact Me</h2>
           <form id="contact-me-form">
           <div>
           <label> Name: </label>
             <input type="text" placeholder="Enter name" id="name"></input>
           </div>
           <div>
           <label> Email:</label>
             <input type="email" placeholder="Enter email" id="email"></input>
           </div>
           <div>
           <label> Message:</label>
             <textarea placeholder="Enter your message here..." id="msg"></textarea>
           </div>
            
        <button> Send </button>
           </form>  
        </section>
     
        <section class="section-style" id="admin-login"><!--Container tag--> 
        <h2>Admin Login</h2>
          <form id="admin-form">
           <div>
           <label> Username: </label>
             <input type="text" placeholder="Enter username" id="usrnme"></input>
           </div>
           <div>
           <label> Password:</label>
             <input type="password" placeholder="Enter password" id="pwd"></input>
           </div>
        <button> Submit </button>
           </form>  
        </section>
<section class="section-style" id="user-responses">
  <h2> User Responses </h2>
  
</section>
         </main>
    </body>
</html>

 CSS

 header {
  background-color: #1279f0;
  border-top:10px solid #28c2f7;
  border-left:10px solid #28c2f7;
  border-right:10px solid #28c2f7;
  text-align:center;
  padding-top:50px;
  border-radius:8px;
}
.one-line{
  border-bottom:10px solid #28c2f7;
  border-radius:8px;
}
.section-style {
  background-color: #fff;
  padding: 3rem 2rem;/*rem means relative size wrt to parent element*/
  border-radius: 8px;
  box-shadow: 0 0 30px rgba(0,0,0,0.3)
}
.section-style h2 {
  color: #1279f0;
  border-bottom: 2px solid #3498db;
  padding-botto: 0.5rem;
  margin-bottom: 1.5rem;
}

nav {
  background-color: #2c3e50;
  padding: 1rem 0;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style-type: none;
  cursor: pointer;
}

nav ul li a {
  color: #fff;
  font-weight: bold;
  margin: 0 15px;/*if not mentioning the specfic side like(margin-left)(margin-right)(margin-top)(margin-bottom) and taking only margin then there exists two values where the first value is for left-right alignment and second value is for top-bottom alignment*/
 text-decoration: none; 
}
nav ul li a:hover{
  color: #28d1f7;
  font-size: 18px;
  border: 2px;
  border-style: solid;
  border-color: #28f7e7;
  border-radius: 6px;
  padding: 2px;
}
#switch-theme {
  position: fixed;
  top: 20px;
  right: 20px;
  background-color: #2c3e50;
  color: #fff;
  border-radius: 8px;
  transition: background-color 0.3s ease;
}

#switch-theme:hover {
  background-color: #3498db;
}

.dark-theme {
  background-color: #34495c;
  color: #3e3d40;
}

.dark-theme header {
  background-color: #34455e;
  color:#ffffff;
}

.dark-theme nav {
  background-theme: #35566e;
}

#admin-login{
  display: none;
}

#user-responses{
  display: none;
}

JAVASCRIPT

let controlOfAdminLogin = document.getElementById("admin-login");

function showAdminLogin() {
  controlOfAdminLogin.style.display = "block";
}

//TASK 2 - MAKE TOGGLE BUTTON WORK
let controlOfThemeBtn = document.getElementById("switch-theme");

controlOfThemeBtn.addEventListener('click', function(){
document.body.classList.toggle("dark-theme");
});

//TASK 3 - Make your Admin Login work.
let controlOfAdminForm = document.getElementById("admin-form");

controlOfAdminForm.addEventListener('submit', function(e){
  e.preventDefault();
  let storedUsername = "admin";
  let storedPassword =  "password";
  
  let username = document.getElementById("usrnme").value;
  let password = document.getElementById("pwd").value;
  
  //LOGIC GATES?? (AND OR NOT)
  //AND - BOTH conditions SHOULD be TRUE -> TRUE SYMBOL -> &&
  //OR - Even if ONE condition is TRUE -> TRUE SYMBOL -> ||
  //NOT - INVERT your decision SYMBOL -> !
  // 2 equal signs 1 with "1" -> TRUE
  //3 equal signs 1 with "1" -> FALSE
  if (storedUsername == username && storedPassword == password) {
    alert("Welcome Admin!");
    
    document.getElementById("admin-login").style.display = "none";
    document.getElementById("user-responses").style.display = "block";
    
    //Call the function which will get user response from the backend in JSON format
    // and display them one by one
    displayUserMessages();
  }
  else {
    alert("Access denied!!");
  }
});

//TASK 4 - Store user response from the contact me section in a backend(Chrome LocalStorage)

let controlOfContactmeForm = document.getElementById("contact-me-form");

controlOfContactmeForm.addEventListener('submit', function(e){
  e.preventDefault();
  
  let name = document.getElementById("name").value;
  let email = document.getElementById("email").value;
  let message = document.getElementById("msg").value;
  let date = new Date().toLocaleString(); //We are getting the date from the system
  
  //Convert these into an Object- Response Object 
  //Why? so we can send it to the backend
  //and to keep a standard way of storing this data.
  
  let response = {
    name, email, message, date
  }
  
 
  
  //Once you run this code for the first time, you will create a Dummy DB in the LocalStorage , every other time there is no need to create it again.
   
  
  //JSON.parse converts JSON structure to JAVASCRIPT Object (Getting data from DB), DB sends you data in JSON format.
  
  //JSON.stringify convert JAVASCRIPT Object to JSON (Sending data from JS to DB, need to converted to JSON)
  let DummyDatabase = JSON.parse(localStorage.getItem('tempDB')) || [ ]; //This will act like or Dummy Database (Actually a list that will be stored in the LocalStorage of Chrome Browser)
  
  //This is how we put item in a JS LIST
  DummyDatabase.push(response) // This still works on JS
  
  
  
  //This is where the tempDB list will go to the backend and start acting as our DummyDatabase.
  localStorage.setItem('tempDB', JSON.stringify(DummyDatabase));
  alert("Thank you for your message, will get back to you shortly!");
  this.reset();
});


function displayUserMessages(){
  //get all responses from the dummy database and show them in the UI on user responses section(After admin login has correct creds.)
  let ControlOfUserMessages = document.getElementById("user-messages");
  
  let DummyDatabase = JSON.parse(localStorage.getItem('tempDB')) || [ ];
  
  DummyDatabase.forEach(response=>{
    let ControlOfResponseElement = document.createElement('div');
    
    ControlOfResponseElement.innerHTML = `
    <p> Name: ${response.name} </p>
    <p> Email: ${response.email} </p>
    <p> Message: ${response.message} </p>
    <p> Date: ${response.date} </p>
    <hr>
    `
    ControlOfUserMessages.append(ControlOfResponseElement);
  });
}

      </main>
    </body>
</html>
