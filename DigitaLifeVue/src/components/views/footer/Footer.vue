<template>
<footer id="footer" class="section footer">
   <div class="container-footer">
      <div class="footer-top">
         <div class="footer-top-box">
            <h3>Know About Us</h3>
            <a href="https://atehno.md/spage/delivery-menu">Shipping and payment</a>
            <a href="https://atehno.md/spage/contacts-menu">Contacts and working hours</a>
            <a href="https://service.atehno.md/">Service-center</a>
            <a href="https://atehno.md/spage/service_centres">Authorized service centers</a>
            <a href="https://atehno.md/spage/credit-menu">Buy in credit</a>
         </div>
         <div class="footer-top-box">
            <h3>Contact Us</h3>
            <a href="https://vk.com/wall17263054_102"><em class="fa fa-vk"></em> VK</a>
            <a href="https://www.facebook.com/usarb.balti/"><em class="fa fa-facebook"></em> Facebook</a>
            <a href="https://www.instagram.com/explore/tags/usarb/"><em class="fa fa-instagram"></em>
            Instagram</a>
            <a href="https://www.youtube.com/channel/UC1s0JOdKAC_26tswxf7wZCQ"><em class="fa fa-youtube"></em>
            YouTube</a>
         </div>
         <div class="footer-top-box">
            <h3>Office Address</h3>
            <div>
               <span>
               <em class="fa fa-map-marker"></em>
               </span>
               Str. Pușkin, nr. 38, MD-3100 Bălți
            </div>
            <div>
               <span>
               <em class="fa fa-plane"></em>
               </span>
               Moldova, Bălți
            </div>
            <div>
               <span>
               <em class="fa fa-phone"></em>
               </span>
               Phone No : +373 231 52430
            </div>
            <div>
               <span>
               <em class="fa fa-envelope"></em>
               </span>
               anticamera@usarb.md
            </div>
         </div>
      </div>
   </div>
   <div class="footer-bottom">
      <div class="footer-bottom-box"></div>
      <div class="footer-bottom-box"></div>
   </div>
</footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>   
.footer {
	margin-top: -300px;
	background-color: #333;
	padding: 50px 20%;
	line-height: 30px;
}

.footer-top-box span,
a {
	text-decoration: none;
	margin-right: 10px;
}

.footer-top {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	color: grey;
}

.footer-top-box a:link,
.footer-top-box a:visited {
	display: block;
	color: white;
	font-size: 14px;
	transition: 0.6s;
}

.footer-top-box a:hover {
	color: rgb(166, 0, 0);
}

.footer-top-box div {
	color: white;
	font-size: 12px;
}

.footer-top-box h3 {
	font-size: 1.8rem;
	font-weight: 400;
	margin-bottom: 1rem;
}

@media only screen and (max-width: 998px) {
	.footer-top {
		grid-template-columns: repeat(2, 1fr);
		row-gap: 2rem;
	}
}

@media only screen and (max-width: 768px) {
	.footer-top {
		grid-template-columns: 1fr;
		row-gap: 2rem;
	}
	@media screen and (max-width: 768px) {
		.footer-top-box h3 {
			font-size: 1.6rem;
		}
	}
	@media screen and (max-width: 400px) {
		.footer-top-box h3 {
			font-size: 1.4rem;
		}
	}
}

@media only screen and (max-width: 1790px) {
	.footer {
		margin-top: 2%;
	}
	.containers {
		margin: 0;
	}
}
</style>