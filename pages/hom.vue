<template>
<main>
<nav class="navbar navbar-expand-lg navbar-dark" style="background: #32CD32;">
                <a class="navbar-brand" href="#" style="color: white;">Bycorp</a>
                        <div class="collapse navbar-collapse" id="navbarSupportedContent">
                            <ul class="navbar-nav mr-auto">
                                <li class="nav-item active">
                                    <NuxtLink to="/hom" class="text-white cd-md-3">
                                        Home
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/product" class="text-white col-md-3">
                                        Product
                                    </NuxtLink>
                                </li>
                                <li class="nav-item active">
                                    <NuxtLink to="/contact" class="text-white col-md-3">
                                        Contact
                                    </NuxtLink>
                                </li>
                            </ul>
                        </div>
            </nav>
<section>
  <img class="mySlides" src="../static/asset/4.jpg"
  style="width:100%">
  <img class="mySlides" src="../static/asset/2.jpg"
  style="width:100%">
  <img class="mySlides" src="../static/asset/3.jpg"
  style="width:100%">
  
</section>
<script>
// Automatic Slideshow - change image every 3 seconds
var myIndex = 0;
carousel();

function carousel() {
    var i;
    var x = document.getElementsByClassName("mySlides");
    for (i = 0; i < x.length; i++) {
       x[i].style.display = "none";
    }
    myIndex++;
    if (myIndex > x.length) {myIndex = 1}
    x[myIndex-1].style.display = "block";
    setTimeout(carousel, 3000);
}
</script>
</main>
</template>