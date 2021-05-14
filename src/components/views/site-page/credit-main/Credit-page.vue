<template>
<main id="main">
   <div class="containers">
      <h1>Purchase on credit</h1>
      <h4>Buying on credit is easy! Check out the terms offered by our partner banks</h4>
      <div style="overflow-x:auto;">
         <table>
            <tr>
               <th>Bank</th>
               <th>Credit Package</th>
               <th>Time, Months</th>
               <th>Syma, Lei</th>
               <th>Commission</th>
               <th>Additional information</th>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"0.00% for 5 months"</td>
               <td>4</td>
               <td>1 000-100 000</td>
               <td>Shop commission 6.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"0.00% for 6 months"</td>
               <td>6</td>
               <td>1 000-100 000</td>
               <td>Shop commission 7.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"0.00% for 10 months"</td>
               <td>10</td>
               <td>1 000-100 000</td>
               <td>Shop commission 11.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"0.00% for 12 months"</td>
               <td>12</td>
               <td>1 000-100 000</td>
               <td>Shop commission 13.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"0.00% for 15 months"</td>
               <td>15</td>
               <td>1 000-100 000</td>
               <td>Shop commission 16.85%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit1.png')" alt=""></td>
               <td>"12.00% for 6-36 months"</td>
               <td>6-36</td>
               <td>1 000-100 000</td>
               <td>Shop commission 1.55%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit2.png')" alt=""></td>
               <td>"0.00% for 3-6 months"</td>
               <td>3-6</td>
               <td>1 000-100 000</td>
               <td>Shop commission 9.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit2.png')" alt=""></td>
               <td>"0.00% for 7-10 months"</td>
               <td>7-10</td>
               <td>1 000-100 000</td>
               <td>Shop commission 13.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit2.png')" alt=""></td>
               <td>"0.00% for 11-12 months"</td>
               <td>11-12</td>
               <td>1 000-100 000</td>
               <td>Shop commission 15.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit2.png')" alt=""></td>
               <td>"0.00% for 13-15 months"</td>
               <td>13-15</td>
               <td>1 000-100 000</td>
               <td>Shop commission 20.0%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
            <tr>
               <td><img :src="require('../../../../../static/img/credit2.png')" alt=""></td>
               <td>"20.00% for 6-36 months"</td>
               <td>6-36</td>
               <td>1 000-100 000</td>
               <td>Shop commission 0.5%</td>
               <td>Unique opportunity: receiving goods at the time of signing a loan agreement</td>
            </tr>
         </table>
      </div>
  </div>
</main>
</template>

<script>
    export default {
        name: "CreditPage"
    }
</script>

<style scoped>
#main {
	margin-top: 0;
}

.containers {
	margin: 17%;
	margin-top: 10px;
}

table {
	font-family: arial, sans-serif;
	border-collapse: collapse;
	width: 100%;
}

td,
th {
	border: 1px solid #dddddd;
	text-align: center;
	padding: 8px;
}

body {
	font-family: Arial, Helvetica, sans-serif;
}

* {
	box-sizing: border-box;
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