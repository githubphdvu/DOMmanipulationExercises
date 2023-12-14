<!DOCTYPE html><!--given HTML-->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>DOM Manipulation Exercises</title>
    <style>
        .header, .footer {
          background-color: gray;
          padding: 10px;
          margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div class="header"></div>
    <section id="container">
        <ul>
            <li class="first">one</li>
            <li class="second">two</li>
            <li class="third">three</li>
        </ul>
        <ol>
            <li class="first">one</li>
            <li class="second">two</li>
            <li class="third">three</li>
        </ol>
    </section>
    <div class="footer"></div>

    <script>
      document.getElementById("container") // 1. Select id container without using querySelector
      document.querySelector("#container") // 2. Select id container using querySelector
      document.getElementsByClassName("second") // 3. Select class second, or...
      // document.querySelectorAll(".second")
      document.querySelector("ol .third") // 4. Select class third and inside ol
      // let foundDiv=document.querySelector("#container").innerText="Hello"//5. Give ele id container text “Hello!”
      let footer = document.querySelector(".footer").classList.add("main")//6.Add class main to div class footer, or
      // footer.className += " main"
      document.querySelector(".footer").classList.remove("main") // 7. Remove class main from class footer
      let newLi = document.createElement("li") // 8. Create li
      newLi.textContent = "four" // 9. Give li text “four”
      let list = document.querySelector("ul").appendChild(newLi) // 10. Append it to ul
      
      let liInsideOl = document.querySelectorAll("ol li")
      for (let i = 0; i < liInsideOl.length; i++) { // 11. Loop over all li inside ol and give them backgroundColor “green”
        liInsideOl[i].style.backgroundColor = "green"
      }
      
      // let footerToRemove = document.querySelector(".footer").remove() // 12. Remove div with class footer
    </script>
</body>
</html>
