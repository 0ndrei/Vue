<template>
  <div class="containers">
   <section>
      <h1>Contact</h1>
      <img class="imgcontact" src="https://enter.online/images/companies/1/Contacts/contacts_entr.webp" alt="">
      <div class="grid-container">
         <div class="item1">
            <h2>Online Store</h2>
            <hr>
            <ul>
               <li><br><em class="fa fa-phone" aria-hidden="true"></em> +373 231 63090</li>
               <li class="email"><br><em class="fa fa-envelope" aria-hidden="true"></em> info@atehno.md</li>
               <li><br><em class="fa fa-clock" aria-hidden="true"></em> Schedule: Monday-Friday: 09:00 - 19:00 | Saturday: 09:00- 18:00 | Sunday: 09:00- 17:00
               </li>
            </ul>
         </div>
         <div class="item2">
            <h2>Corporate Sales</h2>
            <hr>
            <ul>
               <li><br><em class="fa fa-phone" aria-hidden="true"></em> +373 698 34025</li>
               <li class="email"><br><em class="fa fa-envelope" aria-hidden="true"></em> ipetrov@atehno.md</li>
               <li><br><em class="fa fa-clock" aria-hidden="true"></em> Schedule: Monday-Friday: 09:00 - 19:00 | Saturday: 09:00- 18:00 | Sunday: output
               </li>
            </ul>
         </div>
         <div class="item3">
            <h2>Service-center</h2>
            <hr>
            <ul>
               <li><br><em class="fa fa-map-marker" aria-hidden="true"></em> Moldova, Balti, Stefan cel Mare 76a.</li>
               <li><br><em class="fa fa-phone" aria-hidden="true"></em> +373 231 63132</li>
               <li class="email"><br><em class="fa fa-envelope" aria-hidden="true"></em> service@atehno.md</li>
               <li><br><em class="fa fa-clock" aria-hidden="true"></em> Schedule: Monday-Friday: 09:00 - 19:00 | Saturday: 09:00- 18:00 | Sunday: output
               </li>
            </ul>
         </div>
         <div class="item4">
            <h2>Company office</h2>
            <hr>
            <ul>
               <li><br><em class="fa fa-map-marker" aria-hidden="true"></em> Moldova, Balti, Stefan cel Mare 76a.</li>
               <li class="email"><br><em class="fa fa-envelope" aria-hidden="true"></em> info@atehno.md</li>
               <li><br><em class="fa fa-clock" aria-hidden="true"></em> Schedule: Monday-Friday: 09:00 - 19:00 | Saturday: 09:00- 18:00 | Sunday: output
               </li>
            </ul>
         </div>
      </div>
      <iframe
         title="map" src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d36710.46750896094!2d27.891060449999998!3d47.7612147!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e1!3m2!1sru!2s!4v1577443074188!5m2!1sru!2s"></iframe>
   </section>
</div>
</template>

<script>
    export default {
        name: "ContactPage"
    }
</script>

<style scoped>
.containers {
	margin: 17%;
	margin-top: 10px;
}

.grid-container {
	display: grid;
	grid-template-columns: 1fr;
	background-color: white;
	padding: 10px;
}

.grid-container>div {
	text-align: center;
	padding: 10px 0;
	font-size: 25px;
}

.grid-container ul {
	font-size: 15px;
	text-align: left;
	list-style: none;
	text-align: left;
}

.email {
	color: #2997ce;
}

iframe {
	width: 100%;
	height: 500px;
}

.imgcontact {
	width: 100%;
}

@media only screen and (max-width: 1790px) {
	.containers {
		margin: 0;
	}
}

@media only screen and (max-width: 800px) {
	.containers {
		margin: 0;
	}
}
</style>