:root {
  --primary-color: #e50914;
  --dark-color: #141414;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Arial", sans-serif;
  -webkit-font-smoothing: antialiased;
  background: #000;
  color: #999;
}

ul {
  list-style: none;
}

h1,
h2,
h3,
h4 {
  color: #fff;
}

a {
  color: #fff;
  text-decoration: none;
}

p {
  margin: 0.5rem 0;
}

img {
  width: 100%;
}

.showcase {
  width: 100%;
  height: 100vh;
  position: relative;
  background: url("../img/background.jpg") no-repeat center center/cover;
}

.showcase::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  background: rgba(0, 0, 0, 0.6);
  box-shadow: inset 120px 100px 250px #000, inset -120px -100px 250px #000;
}

.showcase-top {
  position: relative;
  height: 90px;
  z-index: 2;
}

.showcase-top img {
  width: 170px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.showcase-top a {
  position: absolute;
  top: 50%;
  right: 0;
  transform: translate(-50%, -50%);
}

.showcase-content {
  position: relative;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 9rem;
  z-index: 2;
}

.showcase-content h1 {
  font-weight: 600;
  font-size: 4rem;
  line-height: 1.1;
  margin: 0 0 2rem 0;
}

.showcase-content p {
  text-transform: uppercase;
  color: #fff;
  font-weight: 400;
  font-size: 1.9rem;
  line-height: 1.1;
  margin: 0 0 2rem;
}

/* Utility Classes */

/* Tabs */
.tabs {
  background: var(--dark-color);
  padding-top: 1rem;
  border-bottom: 3px solid #3d3d3d;
}

.tabs .container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 1rem;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.tabs p {
  font-size: 1.2rem;
  padding-top: 0.5rem;
}

.tabs .container > div {
  padding: 1.5rem 0;
}

.tabs .container > div:hover {
  color: #fff;
  cursor: pointer;
}

.tab-border {
  border-bottom: var(--primary-color) 4px solid;
}

/* Tab Content */
.tab-content {
  padding: 3rem 0;
  background: #000;
  color: #fff;
}

/*  Hide content Initially  */
#tab-1-content,
#tab-2-content,
#tab-3-content {
  display: none;
}

.show {
  display: block !important;
}

#tab-1-content .tab-1-content-inner {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 2rem;
  align-items: center;
  justify-content: center;
}

#tab-2-content .tab-2-content-top {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-gap: 1rem;
  justify-content: center;
  align-items: center;
}

#tab-2-content .tab-2-content-bottom {
  margin-top: 2rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 2rem;
  justify-content: center;
  align-items: center;
  text-align: center;
}

/*  Table  */
.table {
  width: 100%;
  margin-top: 2rem;
  border-collapse: collapse;
  border-spacing: 0;
}

.table thead th {
  text-transform: uppercase;
  padding: 0.8rem;
}

.table tbody tr td {
  color: #999;
  padding: 0.8rem 1.2rem;
  text-align: center;
}

.table tbody tr td:first-child {
  text-align: left;
}

.table tbody tr:nth-child(odd) {
  background: #222;
}

/* Footer */
.footer {
  max-width: 75%;
  margin: 1rem auto;
  overflow: auto;
}

.footer,
.footer a {
  color: #999;
  font-size: 0.9rem;
}

.footer p {
  margin-bottom: 1.5rem;
}

.footer .footer-cols {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 2rem;
}

.footer li {
  line-height: 1.9;
}

/*  Container  */
.container {
  max-width: 70%;
  margin: auto;
  overflow: hidden;
  padding: 0 2rem;
}

/* Text Styles */
.text-xl {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.text-lg {
  font-size: 1.8rem;
  margin-bottom: 1rem;
}

.text-md {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.text-center {
  text-align: center;
}

.text-dark {
  color: #999;
}

/* Buttons */
.btn {
  display: inline-block;
  background: var(--primary-color);
  color: #fff;
  padding: 0.4rem 1.3rem;
  font-size: 1rem;
  text-align: center;
  border: none;
  cursor: pointer;
  margin-right: 0.5rem;
  outline: none;
  box-shadow: 0 1px 0 rgba(0, 0, 0, 0.45);
  border-radius: 2px;
}

.btn:hover {
  opacity: 0.9;
}

.btn-rounded {
  border-radius: 5px;
}

.btn-xl {
  font-size: 1.6rem;
  padding: 1.5rem 2.1rem;
  text-transform: uppercase;
}

.btn-lg {
  font-size: 1.5rem;
  padding: 1.2rem 1.7rem;
  text-transform: uppercase;
}

.btn-icon {
  margin-left: 0.5rem;
}

/*  Media Queries  */
@media (max-width: 960px) {
  .showcase {
    height: 100vh;
  }

  .hide-sm {
    display: none;
  }

  .showcase-top img {
    top: 30%;
    left: 5%;
    transform: translate(0);
  }

  .showcase-top a {
    top: 30%;
    right: 5%;
    transform: translate(0);
  }

  .showcase-content h1 {
    font-size: 2rem;
    line-height: 0.5;
  }

  .showcase-content p {
    font-size: 1rem;
  }

  .footer .footer-cols {
    grid-template-columns: repeat(2, 1fr);
  }

  .btn-xl {
    font-size: 1rem;
    padding: 1rem 1.2rem;
  }

  .btn-lg {
    font-size: 0.8rem;
    padding: 0.8rem 1rem;
  }

  .text-xl {
    font-size: 1.5rem;
  }

  .text-lg {
    font-size: 1.2rem;
  }

  .text-md {
    font-size: 1rem;
  }
}

@media (max-width: 700px) {
  .showcase::after {
    box-shadow: inset 50px 50px 150px #000, inset -50px -50px 150px #000;
  }

  .container {
    max-width: 90%;
    margin: auto;
    overflow: hidden;
    padding: 0px 0.1rem;
  }

  #tab-1-content .tab-1-content-inner {
    grid-template-columns: 1fr;
    text-align: center;
  }

  #tab-2-content .tab-2-content-top {
    display: block;
    text-align: center;
  }

  #tab-2-content .tab-2-content-bottom {
    grid-template-columns: 1fr;
  }

  .btn-lg {
    font-size: 1rem;
    padding: 0.8rem 1rem;
    text-transform: uppercase;
  }

  .tab-item > i {
    font-size: 1.3rem;
  }

  .footer .footer-cols {
    grid-template-columns: 1fr;
  }
}
