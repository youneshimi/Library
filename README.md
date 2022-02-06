# UEMF-Library
Le projet UEMF Library Management System est une application Web développée sur la plate-forme javascript .  Il s'agit d'un  projet de niveau simple et basique à
des fins d'apprentissage.
Cette application Web est développé à l'aide de Html CSS JavaScript et la base de données est automatiquement importée.

## index.html

```ts
<!DOCTYPE html>
<html lang="en">
  <head>
    
    <meta charset="utf-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1, shrink-to-fit=no"
    />
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
      integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T"
     
     
    />
    <link
    rel="stylesheet"
    href="https://use.fontawesome.com/releases/v5.6.3/css/all.css"
    integrity="sha384-UHRtZLI+pbxtHCWp1t77Bi1L4ZtiqrqD80Kn4Z8NTSRyMA2Fd33n5dQ8lWUE00s/"
    
  />
    
    <link rel="stylesheet" href="style.css" />
    <title>UEMF library</title>

  </head>
  <body style="background-image: url('');
  background-repeat: repeat; background-color: rgba(236, 236, 236, 0.842); background-blend-mode: lighten;">
    <nav class="navbar navbar-expand-lg navbar-light bg-info">
      <a class="navbar-brand ml-4" href="#"><img src="assets/Favicons/3.png" alt="vibe Library" class="logo-img"></a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="#"
              >Home <span class="sr-only">(current)</span></a
            >
          </li>
          <li class="nav-item"><a href="./book.html" class="nav-link">free library
          </a></li>
        </ul>
        <form class="form-inline my-2 my-lg-0">
          <input
            class="form-control mr-sm-2"
            id="searchTxt"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn btn-dark my-2 my-sm-0" type="submit">
            Search
          </button>
        </form>
      </div>
    </nav>

    <div id="message"></div>

    <div class="container my-3">
      <h1>UEMF Library</h1>
      <h5 align="center">
        <a href="" style="color:black;" class="typewrite" data-period="2000" 
        data-type='[ "Study time, crunch time, anytime" ]'>
          <span class="wrap"></span>
        </a>
      </h5>
      <hr />
      <form id="libraryForm">
        <div class="form-group row">
          <label for="bookName" class="col-sm-2 col-form-label">Name</label>
          <div class="col-sm-10">
            <input
              type="text"
              class="input-box"
              id="bookName"
              placeholder="Book Name"
            />
          </div>
        </div>
        <div class="form-group row">
          <label for="Author" class="col-sm-2 col-form-label">Author</label>
          <div class="col-sm-10">
            <input
              type="text"
              class="input-box"
              id="author"
              placeholder="Author"
            />
          </div>
        </div>
        <fieldset class="form-group">
          <div class="row">
            <legend class="col-form-label col-sm-2 pt-0">Category</legend>

            <div class="col-sm-10">
               
                <div class="form-check">

                  <select class="form-check-input" name="type" id="type">

                    
                    <option value="N/A">Select Category</option>
                    <option value="Arts & Music">Arts & Music</option>
                    <option value="Biographies">Biographies</option>
                    <option value="Business">Business</option>
                    <option value="Comics">Comics</option>
                    <option value="Computer & Tech">Computers & Tech</option>
                    <option value="Cooking">Cooking</option>
                    <option value="Education & Reference">Education & Reference</option>
                    <option value="Entertainment">Entertainment</option>
                    <option value="Health & Fitness">Health & Fitness</option>
                    <option value="History">History</option>
                    <option value="Hobbies & Crafts">Hobbies & Crafts</option>
                    <option value="Home & Garden">Home & Garden</option>
                    <option value="Horror">Horror</option>
                    <option value="Kids">Kids</option>
                    <option value="Literature & Fiction">Literature & Fiction</option>
                    <option value="Medical">Medical</option>
                    <option value="Mystery">Mystery</option>
                    <option value="Parenting">Parenting</option>
                    <option value="Religion">Religion</option>
                    <option value="Romance">Romance</option>
                    <option value="Sci-Fi & Fantasy">Sci-Fi & Fantasy</option>
                    <option value="Science & Maths">Science & Maths</option>
                    <option value="Self-Help">Self-Help</option>
                    <option value="Social Sciences">Social Sciences</option>
                    <option value="Sports">Sports</option>
                    <option value="Travel">Travel</option>
                    <option value="True Crime">True Crime</option>
                   
                
                  </select>
                </div>
            </div>
          </div>
        </fieldset>

        <div class="form-group row">
          <div class="col-sm-10">
            <button type="submit" class="btn btn-primary">Add Book</button>
          </div>
        </div>
      </form>

      <div id="table">
        <h1>Your books</h1>

        <table class="table table-striped">
          <thead>
            <tr>
              <th scope="col">Name</th>
              <th scope="col">Author</th>

              <th scope="col">Type</th>
              <th scope="col">Category</th>

              <th scope="col"></th>
            </tr>
          </thead>
          <tbody id="tableBody"></tbody>
        </table>
      </div>
    </div>
   <div >
  
    <script src="script.js"></script>
    <script
      src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
      integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
      
    ></script>
    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"
      integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1"
      
    ></script>
    <script
      src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"
      integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM"
      
    ></script>
  </body>
</html>

```

> `Balises méta obligatoires`
```ts
 <meta charset="utf-8" />
    <meta
```
> `Bootstrap CSS`
```ts
    <link
      rel="stylesheet"
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css"
      integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T"
      crossorigin="anonymous"
    />
```        
> **Font Awesome**

**A quoi sert Font Awesome ?**

Font Awesome est une police d'écriture et un outil d'icônes qui se base sur `CSS`
est aussi un ensemble d'icônes largement utilisé qui vous donne des images vectorielles évolutives pouvant être personnalisées avec `“Cascading Style Sheets”` 

```ts
    <link
    rel="stylesheet"
    href="https://use.fontawesome.com/releases/v5.6.3/css/all.css"
    integrity="sha384-UHRtZLI+pbxtHCWp1t77Bi1L4ZtiqrqD80Kn4Z8NTSRyMA2Fd33n5dQ8lWUE00s/"
    
  />
```

> Déclaration du Style CSS 
```ts
    <link rel="stylesheet" href="style.css" />
```    


> jQuery

```ts
<script
      src="https://code.jquery.com/jquery-3.3.1.slim.min.js"
      integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo"
 ```     
    ></script>
    
> Popper.js

```ts
<script
      src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"
      integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1"
      
    ></script>
```    
> Bootstrap JS 

```ts
    <script
      src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"
      integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM"
      
    ></script>
```

> **Choix de catégorie**

```ts

                    
                    <option value="N/A">Select Category</option>
                    <option value="Arts & Music">Arts & Music</option>
                    <option value="Biographies">Biographies</option>
                    <option value="Business">Business</option>
                    <option value="Comics">Comics</option>
                    <option value="Computer & Tech">Computers & Tech</option>
                    <option value="Cooking">Cooking</option>
                    <option value="Education & Reference">Education & Reference</option>
                    <option value="Entertainment">Entertainment</option>
                    <option value="Health & Fitness">Health & Fitness</option>
                    <option value="History">History</option>
                    <option value="Hobbies & Crafts">Hobbies & Crafts</option>
                    <option value="Home & Garden">Home & Garden</option>
                    <option value="Horror">Horror</option>
                    <option value="Kids">Kids</option>
                    <option value="Literature & Fiction">Literature & Fiction</option>
                    <option value="Medical">Medical</option>
                    <option value="Mystery">Mystery</option>
                    <option value="Parenting">Parenting</option>
                    <option value="Religion">Religion</option>
                    <option value="Romance">Romance</option>
                    <option value="Sci-Fi & Fantasy">Sci-Fi & Fantasy</option>
                    <option value="Science & Maths">Science & Maths</option>
                    <option value="Self-Help">Self-Help</option>
                    <option value="Social Sciences">Social Sciences</option>
                    <option value="Sports">Sports</option>
                    <option value="Travel">Travel</option>
                    <option value="True Crime">True Crime</option>
                   
```  


![index](https://user-images.githubusercontent.com/96379214/152663398-858be577-4fd3-4d48-aa4f-86963098e29d.png)




## Script.js

```ts
function Book(name, author, type) {
  this.name = name;
  this.author = author;
  this.type = type;
}

var TxtType = function(el, toRotate, period) {
  this.toRotate = toRotate;
  this.el = el;
  this.loopNum = 0;
  this.period = parseInt(period, 10) || 2000;
  this.txt = '';
  this.tick();
  this.isDeleting = false;
};

TxtType.prototype.tick = function() {
  var i = this.loopNum % this.toRotate.length;
  var fullTxt = this.toRotate[i];

  if (this.isDeleting) {
  this.txt = fullTxt.substring(0, this.txt.length - 1);
  } else {
  this.txt = fullTxt.substring(0, this.txt.length + 1);
  }

  this.el.innerHTML = '<span class="wrap">'+this.txt+'</span>';

  var that = this;
  var delta = 200 - Math.random() * 100;

  if (this.isDeleting) { delta /= 2; }

  if (!this.isDeleting && this.txt === fullTxt) {
  delta = this.period;
  this.isDeleting = true;
  } else if (this.isDeleting && this.txt === '') {
  this.isDeleting = false;
  this.loopNum++;
  delta = 500;
  }

  setTimeout(function() {
  that.tick();
  }, delta);
};

window.onload = function() {
  var elements = document.getElementsByClassName('typewrite');
  for (var i=0; i<elements.length; i++) {
      var toRotate = elements[i].getAttribute('data-type');
      var period = elements[i].getAttribute('data-period');
      if (toRotate) {
        new TxtType(elements[i], JSON.parse(toRotate), period);
      }
  }
  var css = document.createElement("style");
  css.type = "text/css";
  css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
  document.body.appendChild(css);
};


function Display() {}

let countBooks = 0;
Display.prototype.add = function (book) {
  console.log("Adding to UI");
  tableBody = document.getElementById("tableBody");
  countBooks = countBooks + 1;
  let uiString = `<tr id="${countBooks}">
                        <td>${book.name}</td>
                        <td>${book.author}</td>
                        <td>${book.type}</td>
                        <td><button class="btn btn-success" id="edit" onclick="editfunction('${book.name}','${book.author}','${book.type}','${countBooks}')">Edit</button>
                        </td?
                        <td><button class="btn btn-danger" id="edit" onclick="deletefunction('${countBooks}')">Delete</button>
                        </td>
                    </tr>`;
  tableBody.innerHTML += uiString;
};

Display.prototype.clear = function () {
  let libraryForm = document.getElementById("libraryForm");
  libraryForm.reset();
};

Display.prototype.validate = function (book) {
  if (book.name.length < 2 || book.author.length < 2) {
    return false;
  } else {
    return true;
  }
};
Display.prototype.show = function (type, displayMessage) {
  let message = document.getElementById("message");
  message.innerHTML = `<div class="alert alert-${type} alert-dismissible fade show" role="alert">
                            <strong>Messge:</strong> ${displayMessage}
                            <button type="button" class="close" data-dismiss="alert" aria-label="Close">
                            <span aria-hidden="true">×</span>
                            </button>
                        </div>`;
  setTimeout(function () {
    message.innerHTML = "";
  }, 2000);
};

let libraryForm = document.getElementById("libraryForm");
libraryForm.addEventListener("submit", libraryFormSubmit);

function libraryFormSubmit(e) {
  console.log("YOu have submitted library form");
  let name = document.getElementById("bookName").value;
  let author = document.getElementById("author").value;
  let type = document.getElementById("type").value;
 

  let book = new Book(name, author, type);
  console.log(book);

  let display = new Display();

  if (display.validate(book)) {
    display.add(book);
    display.clear();
    display.show("success", "Your book has been successfully added");
  } else {
    display.show("danger", "Sorry you cannot add this book");
  }

  e.preventDefault();
}

function editfunction(pbookname, pauthorname, ptype, pbookid) {
  document.getElementById("bookName").value = pbookname;
  document.getElementById("author").value = pauthorname;
  document.getElementById(ptype).checked = true;
  document.getElementById(pbookid).style.display = "none";
}
function deletefunction(pbookid) {
  document.getElementById(pbookid).style.display = "none";
}
     
```


> Constructeur

```ts
function Book(name, author, type) {
  this.name = name;
  this.author = author;
  this.type = type;
}
```

> texte de machine à écrire

```ts
var TxtType = function(el, toRotate, period) {
  this.toRotate = toRotate;
  this.el = el;
  this.loopNum = 0;
  this.period = parseInt(period, 10) || 2000;
  this.txt = '';
  this.tick();
  this.isDeleting = false;
};
```
> INJECTION CSS

```ts
var css = document.createElement("style");
  css.type = "text/css";
  css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
  document.body.appendChild(css);
};
```

> Affiche le constructeur

```ts
function Display() {}
```

> Implémente la fonction clear
```ts

Display.prototype.clear = function () {
  let libraryForm = document.getElementById("libraryForm");
  libraryForm.reset();
};
```
> Implémenter la fonction de validation
```ts

Display.prototype.validate = function (book) {
  if (book.name.length < 2 || book.author.length < 2) {
    return false;
  } else {
    return true;
  }
};
```
> Ajoute un écouteur d'événement de soumission à libraryForm

```ts
let libraryForm = document.getElementById("libraryForm");
libraryForm.addEventListener("submit", libraryFormSubmit);
```


> Afficher l'erreur à l'utilisateur

```ts
display.show("danger", "Sorry you cannot add this book");
  }

  e.preventDefault();
}
```

> fonction d'édition

```ts
function editfunction(pbookname, pauthorname, ptype, pbookid) {
  document.getElementById("bookName").value = pbookname;
  document.getElementById("author").value = pauthorname;
  document.getElementById(ptype).checked = true;
  document.getElementById(pbookid).style.display = "none";
}
```

> Suppression fonction

```ts

function deletefunction(pbookid) {
  document.getElementById(pbookid).style.display = "none";
}
     
```

>Ajout de méthodes pour afficher le prototype

```ts
let countBooks = 0;
Display.prototype.add = function (book) {
  console.log("Adding to UI");
  tableBody = document.getElementById("tableBody");
  countBooks = countBooks + 1;
  let uiString = `<tr id="${countBooks}">
                        <td>${book.name}</td>
                        <td>${book.author}</td>
                        <td>${book.type}</td>
                        <td><button class="btn btn-success" id="edit" onclick="editfunction('${book.name}','${book.author}','${book.type}','${countBooks}')">Edit</button>
                        </td?
                        <td><button class="btn btn-danger" id="edit" onclick="deletefunction('${countBooks}')">Delete</button>
                        </td>
                    </tr>`;
  tableBody.innerHTML += uiString;
};
```

## Style.css

```ts
.input-box {
  border: none;
  border-bottom: 1.5px solid rgba(168, 154, 154, 0.322);
  border-radius: 0px;
  transition: none;
  width: 100%;
  padding-bottom: 2px;
}
.input-box:focus {
  outline: none;
  border-bottom: 1.5px solid red;
 
  transform: scaleY(1.05);
}
.input-box {
  transition: border 0.5s ease-out;
  /* transition: transform 0.5s ease-out; */
}


.btn {
    width: 150px;
    height: 50px;
    border: none;
    outline: none;
    color: #fff;
    background: green;
  background-image: -webkit-linear-gradient(top, #5282d4, #28667d);
  background-image: -moz-linear-gradient(top, #5282d4, #28667d);
  background-image: -ms-linear-gradient(top, #5282d4, #28667d);
  background-image: -o-linear-gradient(top, #5282d4, #28667d);
  background-image: linear-gradient(to bottom, #5282d4, #28667d);
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 10px;
    margin-top: 2rem;
}

.btn:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00, #48ff00, #00ffd5, #002bff, #7a00ff, #ff00c8, #ff0000);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity .3s ease-in-out;
    border-radius: 10px;
}

.btn:active {
    color: #000
}

.btn:active:after {
    background: transparent;
}

.btn:hover:before {
    opacity: 1;
}

.btn:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #5282d4;
  background-image: -webkit-linear-gradient(top, #5282d4, #28667d);
  background-image: -moz-linear-gradient(top, #5282d4, #28667d);
  background-image: -ms-linear-gradient(top, #5282d4, #28667d);
  background-image: -o-linear-gradient(top, #5282d4, #28667d);
  background-image: linear-gradient(to bottom, #5282d4, #28667d);
    left: 0;
    top: 0;
    border-radius: 10px;
}

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}

.space {
  margin-top: 10px;
}
footer {
  position: relative;
  width: 100%;
  height: 9vh;
  background-color: rgb(255, 255, 255);
  color: rgb(0, 0, 0);
}
/*  */
.icons ul {
  display: flex;
  margin-top: 190px !important;
}

.icons ul li {
  list-style: none;
}

.icons ul li a {
  width: 40px;
  height: 40px;
  background-color: #fff;
  text-align: center;
  line-height: 35px;
  font-size: 15px;
  margin: 0 10px;
  display: block;
  border-radius: 50%;
  position: relative;
  overflow: hidden;
  border: 3px solid #fff;
  z-index: 1;
  margin-top: 15px;
}

.icons ul li a .icon {
  position: relative;
  color: #262626;
  transition: 0.5s;
  z-index: 3;
}

.icons ul li a:hover .icon {
  color: #fff;
  transform: rotateY(360deg);
}

.icons ul li a:before {
  content: "";
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  height: 100%;
  background: blue;
  transition: 0.5s;
  z-index: 2;
}

.icons ul li a:hover:before {
  top: 0;
}

.icons ul li:nth-child(2) a:before {
  background: black;
}
/* CopyRights */
.icons ul p {
  position: absolute;
  left: 40%;
  top: 20px;
}

.logo-img{
  margin-left: 40px;
  height: 45px;
  width: 80px;
}

@media only screen and (max-width: 500px) {
  .icons ul p {
    position: absolute;
    left: 50%;
    top: 20px;
  }
}

```

## book.html 

```ts
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
    <link rel="stylesheet" href="book.css">
    <title>free library</title>
</head>
<body>
    <div class="home"></div>
    <div class="container">
        <h2 style="text-align: center; padding: 10px 0 10px 0; color: rgb(94, 64, 43);">free library</h2>
        <div class="card card-custom">
            <div class="card-body">
    <form>
        <div class="form-row">
            <div class="form-group col-md-6">
              <label for="inputEmail4">First Name</label>
              <input type="email" class="form-control" id="inputEmail4" placeholder="First Name">
            </div>
            <div class="form-group col-md-6">
              <label for="inputPassword4">Last Name</label>
              <input type="password" class="form-control" id="inputPassword4" placeholder="Last Name">
            </div>
          </div>
        <div class="form-row">
          <div class="form-group col-md-6">
            <label for="inputEmail4">Email</label>
            <input type="email" class="form-control" id="inputEmail4" placeholder="Email">
          </div>
          <div class="form-group col-md-6">
            <label for="inputPassword4">Contact</label>
            <input type="number" class="form-control" id="inputPassword4" placeholder="Contact">
          </div>
        </div>
        <div class="form-group">
          <label for="inputAddress">Address</label>
          <input type="text" class="form-control" id="inputAddress" placeholder="Rte Principale Fès Meknès, Fès">
        </div>
        <div class="form-group">
          <label for="inputAddress2">Address 2</label>
          <input type="text" class="form-control" id="inputAddress2" placeholder="Apartment, studio, or floor">
        </div>
        <div class="form-row">
          <div class="form-group col-md-6">
            <label for="inputCity">City</label>
            <input type="text" class="form-control" id="inputCity">
          </div>
          <div class="form-group col-md-4">
            <label for="inputState">State</label>
            <select id="inputState" class="form-control">
              <option selected>Choose...</option>
              <option>...</option>
            </select>
          </div>
          <div class="form-group col-md-2">
            <label for="inputZip">Zip</label>
            <input type="text" class="form-control" id="inputZip">
          </div>
        </div>
        <div class="form-group">
          <div class="form-check">
            <input class="form-check-input" type="checkbox" id="gridCheck">
            <label class="form-check-label" for="gridCheck">
              Agree to terms and conditions
            </label>
          </div>
        </div>
        <button type="submit" class="btn btn-primary">Donate</button>
        <button type="submit" class="btn btn-primary"><a style="text-decoration: none; color: white;" href="index.html">Back to Home</a></button>
      </form>
    </div>
</div>
</div>

    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
</body>
</html>

```


![book](https://user-images.githubusercontent.com/96379214/152663981-9e99b424-e8dc-49cd-b18d-13406caecbc0.png)

![Projet sans titre](https://user-images.githubusercontent.com/96379214/152665603-669c9a85-4775-4ea1-a241-7619a08a6d72.gif)
