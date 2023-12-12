<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Website Studio</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        background-color: hsl(198, 19%, 90%);
      }

      * {
        box-sizing: border-box;
      }

      header {
        position: relative;
      }

      .menu1 {
        display: block;
        position: absolute;
        right: 0px;
        width: 250px;
        transition: 0.5s;
      }

      .menu1 ul {
        list-style: none;
        text-decoration: none;
        display: flex;
        justify-content: flex-end;
      }

      .menu1 li {
        padding: 15px;
        border-bottom: 1px solid black;
        text-decoration: none;
      }

      .menu1 a {
        text-decoration: none;
      }

      #burger-toggle:checked ~ .menu1 {
        display: block;
        right: 0px;
      }
      #burger-toggle:checked ~ .burger {
        display: none;
        right: 0px;
      }
      #burger-toggle:checked ~ .cross {
        display: block;
        right: 0px;
      }

      .burger .line {
        width: 30px;
        height: 4px;
        background-color: #d0cdcd;
        margin: 5px 0;
      }

      #burger-toggle {
        display: none;
      }

      .burger {
        display: none;
        position: absolute;
        right: 0px;
        z-index: 1;
        margin-right: 5px;
      }
      .cross {
        display: none;
        position: absolute;
        right: 0px;
        z-index: 1;
        margin-right: 15px;
        color: #d0cdcd;
      }

      @media (max-width: 768px) {
        .burger {
          display: block;
        }
        .cross {
          display: none;
        }

        .menu1 {
          background: #1e1d1d;
          right: -100%;
        }

        .menu1 li {
          display: block;
        }

        .menu1 ul {
          display: flex;
          flex-direction: column;
          margin-top: 210px;
        }
      }

      .menu {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        padding: auto;
        background-color: black;
      }
      .logo-image {
        width: 30px;
        height: auto;
        margin: 10px;

        border: 2px solid #007bff;
        border-radius: 10px;
        box-shadow: 3px 3px 5px #888888;
      }
      .menu-items {
        list-style: none;
        margin: 0;
        display: flex;
        color: aqua;
      }
      .menu li {
        margin-right: 20px;
      }

      footer {
        text-align: center;
        padding: 15px;
        background-color: #548a96;
        color: #fff;
      }

      .toggle {
        border: 1px solid grey;
        margin: 20px;
        padding: 10px;
        cursor: pointer;
        background-color: lightgray;
      }
      .panel {
        display: none;
      }
      #about {
        font-size: medium;
        font-weight: 700;
        font-style: italic;
      }
      div.panel {
        font-size: large;
        background-color: antiquewhite;
      }

      .hero {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        /* background-image: url("https://facts.net/wp-content/uploads/2023/05/man-snowboarding.jpeg"); */
        background: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.5)),
          url("https://facts.net/wp-content/uploads/2023/05/man-snowboarding.jpeg");
        background-size: cover; /* This will cover the entire container */
        background-position: center;
      }

      .img-header {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        max-width: 700px;
      }

      .hero h1 {
        font-size: 80px;
        color: #ecedf7;
      }

      .hero div {
        font-size: 30px;
        color: #e9d1ff;
      }

      button {
        font-size: 40px;
        padding: 10px 40px;
        border-radius: 15px;
        border: none;
        background-color: black;
        color: white;
        box-shadow: 3px 3px 5px #888888;
      }
      .services {
        display: flex;
        flex-direction: column;
        align-items: stretch;
        margin-top: 50px;
        margin-left: 15%;
        margin-right: 15%;
      }

      .services h2 {
        align-self: center;
        font-size: 50px;
        text-align: center;
      }
      .services h3 {
        align-self: center;
        font-size: 30px;
      }
      .service {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 50px;
        gap: 50px;
      }

      .reverse {
        flex-direction: row-reverse;
        background-color: rgb(223, 223, 223);
      }
      .services img {
        width: 500px;
        height: 250px;
      }
    </style>
  </head>
  <body>
    <header class="menu">
      <a href="/home" class="logo">
        <img
          src="https://media.licdn.com/dms/image/C4D0BAQEe7Oqy-M7jBQ/company-logo_200_200/0/1638280750854?e=2147483647&v=beta&t=rgqHo1h-U3sMtsFXuRW74FDYbfLkPOikbcKBnM5GkHc"
          alt="Company Logo"
          class="logo-image"
        />
      </a>

      <input type="checkbox" id="burger-toggle" />
      <label for="burger-toggle" class="burger">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </label>

      <label for="burger-toggle" class="cross">
        <p>X</p>
      </label>

      <nav class="menu1">
        <ul class="menu-items">
          <!-- TODO -->
          <li><a href="#home" style="color: white">Home</a></li>
          <li><a href="about" style="color: white">About</a></li>
          <li><a href="#services1" style="color: white">Services</a></li>
          <li><a href="contacts" style="color: white">Contacts</a></li>
          <li>
            <a
              href="https://github.com/suiunbaev-b-auca-2022/githubpages2/blob/main/goals.md"
              style="color: white">Info</a
            >
          </li>
        </ul>
      </nav>
    </header>
    <main>
      <section class="hero">
        <div class="img-header">
          <h1>Creative Website Studio</h1>
          <div>
            The Best Studio that Makes For You Well-Designed and Search Engine
            Optimized Website. Order Right Now and Get a Ready-Made Website in a
            Day!
          </div>
          <p></p>
          <button>Order</button>
        </div>
      </section>

      <section class="services">
        <h2 id="services1">What Services Can We Provide for You?</h2>

        <div class="service">
          <img
            src="https://miro.medium.com/v2/resize:fit:828/format:webp/1*aTYOTFS4Vkr-nwHNML3GvQ.jpeg"
            alt="Sample Image2"
          />
          <div>
            <h3>Web Design</h3>

            Web design refers to the design of websites that are displayed on
            the internet. It usually refers to the user experience aspects of
            website development rather than software development. Web design
            used to be focused on designing websites for desktop browsers;
            however, since the mid-2010s, design for mobile and tablet browsers
            has become ever-increasingly important.
          </div>
        </div>

        <div class="service reverse">
          <img
            src="https://www.postalplussuwanee.com/portals/98/StoreFiles/design2.jpg"
            alt="Sample Image3"
          />
          <div>
            <h3>Graphic Design</h3>
            Graphic design is a craft where professionals create visual content to
            communicate messages. By applying visual hierarchy and page layout techniques,
            designers use typography and pictures to meet users’ specific needs and
            focus on the logic of displaying elements in interactive designs, to
            optimize the user experience.
          </div>
        </div>

        <div class="service">
          <img
            src="https://www.lemonlight.com/wp-content/uploads/2023/01/AdobeStock_275879381-768x485.jpeg"
            alt="Sample Image4"
          />
          <div>
            <h3>Search Engine optimization</h3>
            Search engine optimization (SEO) is the art and science of getting pages
            to rank higher in search engines such as Google. Because search is one
            of the main ways in which people discover content online, ranking higher
            in search engines can lead to an increase in traffic to a website.
          </div>
        </div>
      </section>

      <!-- <div class="toggle" id="about" onclick="toggle()">About Us</div>
      <div class="panel" id="panel">
        A private website development company.
        <p></p>
        <img
          src="https://web.tanais.ru/local/templates/webtns/img/razrab.png"
          alt="Sample Image"
        />
      </div>
      <script>
        function toggle() {
          if (document.getElementById("panel").style.display == "block") {
            document.getElementById("panel").style.display = "none";
          } else {
            document.getElementById("panel").style.display = "block";
          }
        }
      </script> -->

      <!-- <section class="contacts">
        <h2 id="contacts1">Contacts</h2>
        <p>Name: Baitur Suiunbaev</p>
        <p>Organization: BS Company</p>
        <p>Address: 123 Main Street, Suite 456 Cityville, State 78901</p>

        <p>Phone: +996771234567</p>
        <p>Email: contact@mywebsite.com</p>
        <h4>Operating Hours:</h4>
        <p>Monday - Friday: 9:00 AM - 5:00 PM</p>
        <p>Saturday: 10:00 AM - 2:00 PM</p>
        <p>Sunday: Closed</p>
        <h4>Customer Support:</h4>
        <p>Email: support@mywebsite.com</p>
        <p>Phone: +996 (771) 234567</p>
        <h4>Sales Department:</h4>
        <p>Email: sales@mywebsite.com</p>
        <p>Phone: +996 (770) 123456</p>
        <p></p>
      </section> -->
      <li><a href="#home">Go Up</a></li>
    </main>
    <footer>&copy; 2023 My Website</footer>
  </body>
</html>
