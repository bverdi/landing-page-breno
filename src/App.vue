<template>
  <div id="app">
	<div>
	  <b-navbar toggleable="sm" fixed type="light" variant="transparent">

	    <b-navbar-brand href="#"><img id="brand" src="https://s3.amazonaws.com/freecodecamp/original_trombones.png" alt="Original Trombones"></b-navbar-brand>
	   	<b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>

	      <!-- Right aligned nav items -->
	      <b-collapse id="nav-text-collapse" is-nav>
		      <b-navbar-nav class="ml-auto">
				<b-nav-item href="#" v-scroll-to="'#container-features'">Features</b-nav-item>
				<b-nav-item href="#" v-scroll-to="'#container-video'">How it Works</b-nav-item>
				<b-nav-item href="#" v-scroll-to="'#container-prices'">Pricing</b-nav-item>
		      </b-navbar-nav>
	      </b-collapse>
	  </b-navbar>
	</div>
	<div id="container-form">
		<h3> Handcrafted, home-made masterpieces </h3>
		<div role="group">
			<b-form @submit.stop.prevent>
			    <b-form-input
			      id="input-live"
			      type="email"
			      v-model="email"
			      :state="emailState"
			      aria-describedby="input-live-help input-live-feedback"
			      placeholder="Enter your email"
			      trim
			    ></b-form-input>

			    <!-- This will only be shown if the preceding input has an invalid state -->
			    <b-form-invalid-feedback id="input-live-feedback">
			    </b-form-invalid-feedback>
			    <b-button type="submit" variant="warning" id="call-to-action">GET STARTED!</b-button>
		    </b-form>
	 	</div>
	</div>
	<div id="container-features">

	<b-container class="bv-example-row">
	<div class="feature">
		<b-row>
		    <b-col cols="2" md="0"><div class="icon"><font-awesome-icon :icon="['fas', 'fire']" /></div></b-col>
		    <b-col cols="10" md="10"><h2> Premium Materials </h2><p> Our trombones use the shiniest brass which is sourced locally. This will increase the longevity of your purchase. </p> </b-col>
		</b-row>
	</div>
	<div class="feature">
		<b-row>
		    <b-col cols="2" md="0"><div class="icon"><font-awesome-icon :icon="['fas', 'truck']" /></div></b-col>
		    <b-col cols="10" md="10"><h2> Fast Shipping </h2><p> We make sure you recieve your trombone as soon as we have finished making it. We also provide free returns if you are not satisfied. </p> </b-col>
		</b-row>
	</div>
	<div class="feature">
		<b-row>
		    <b-col cols="2" md="0"><div class="icon"><font-awesome-icon :icon="['fas', 'battery-full']" /></div></b-col>
		    <b-col cols="10" md="10"><h2> Quality Assurance </h2><p> For every purchase you make, we will ensure there are no damages or faults and we will check and test the pitch of your instrument. </p> </b-col>
		</b-row>
	</div>
	</b-container>
	</div>
	<div id="container-video">

		<iframe style="max-width: 560px; width: 100%;" height="315" src="https://www.youtube.com/embed/y8Yv4pnO7qc?controls=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


	</div>

<div id="container-prices">
  <b-row>
  <b-col cols="2"></b-col>
  <b-col cols="8">
  <div>
    <b-card-group deck>
      <b-card
        border-variant="dark"
        header="TENOR TROMBONE"
        header-bg-variant="light"
        header-text-variant="black"
        align="center"
      >
                <b-card-text>
        			 <h2> 600$ </h2>
        			 <p> Lorem ipsum. <br>
					 Lorem ipsum. <br>
					 Lorem ipsum dolor. <br>
					 Lorem ipsum. </p></b-card-text>
        <b-button href="#" variant="warning">SELECT</b-button>

      </b-card>

      <b-card
        border-variant="dark"
        header="BASS TROMBONE"
        header-bg-variant="light"
        header-text-variant="black"
        align="center"
      >
        <b-card-text>
        			 <h2> 600$ </h2>
        			 <p> Lorem ipsum. <br>
					 Lorem ipsum. <br>
					 Lorem ipsum dolor. <br>
					 Lorem ipsum. </p></b-card-text>        
					 <b-button href="#" variant="warning">SELECT</b-button>

      </b-card>

      <b-card
        border-variant="dark"
        header="VALVE TROMBONE"
        header-bg-variant="light"
        header-text-variant="black"
        align="center"
      >
        <b-card-text>
        			 <h2> 600$ </h2>
        			 <p> Lorem ipsum. <br>
					 Lorem ipsum. <br>
					 Lorem ipsum dolor. <br>
					 Lorem ipsum. </p></b-card-text>
		<b-button href="#" variant="warning">SELECT</b-button>

      </b-card>
    </b-card-group>
  </div>
  	</b-col>
  	<b-col cols="2"></b-col>
    </b-row>
</div>

<div id="footer">
	<p> Copyright 2016, Original Trombones</p>
</div>

  </div>
</template>
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script src="https://cdn.jsdelivr.net/npm/vue-scrollto"></script>
<script>

export default {
  name: 'app',
    computed: {
      emailState() {
        return this.email.length > 5 && this.email.includes('@') ? true : false
      }
    },
    data() {
      return {
        email: ''
      }
    }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css?family=Lato:400,700&display=swap');

#footer {
	bottom: 0;
	left: 50;
	right: 50;
	margin: 0 auto;
	text-align: center;
	margin: 100px auto 0px auto;
}

@media (max-width: 576px){
	#container-form {
		width: 60% !important;
	}
}

@media (max-width: 443px){

	.navbar-toggler {
	position: absolute !important; 
	left: 10px !important;
	top: 10px !important;
	}

	.navbar-collapse {
		margin-top: 50px !important;
	}

	.navbar-brand {
	position: absolute !important;
	top: 7px !important;
	left: 5% !important;
	}
}

@media (min-width: 768px) {
	.nav-link {
		margin-right: 60px;
	}
}

h2{
	font-weight: bolder !important;
}

#container-features {
	width: 70%;	
	margin: 100px auto 50px auto;
}

#container-prices {

	margin: 100px auto 50px auto;
}

.feature {
	text-align: left;
	margin-top: 50px;
}

.icon {
	font-size: 3em;
	color: orange;
	margin-left: -30px;
}

#call-to-action {
	font-weight: bolder;
	margin-top: 20px;
}

body {
	background-color: palegoldenrod !important;
	font-family: 'Lato', sans-serif;
}

#container-form {
	margin: 60px auto 50px auto;
	width: 30%;
}

#brand {
	width: 100%;
    height: 100%;
    max-width: 300px;
    margin-left: 40px;
}

.nav-link {
	color: black !important;
}

.nav-link:hover {
	text-decoration: underline !important;
}

.item-menus {
	color: black !important;
}

h3 {
	font-weight: bolder !important;
	font-size: 24px !important;
}

#app {
  font-family: 'Lato', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
