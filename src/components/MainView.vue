<template>
	<v-app id="inspire">

        <v-app-bar
			dense
            app
            elevation="0"
            style="display: flex: !important; justify-content: space-between !important;"
            class="d-flex d-sm-flex d-md-none"
        > 
            <a href="/">
                <v-img max-width="160px" src="../assets/Company_gray.png"></v-img>
            </a>
            <v-app-bar-nav-icon class="d-lg-none" id="drawer" @click="drawer = !drawer"></v-app-bar-nav-icon> 
        </v-app-bar>
    
        <v-app-bar
            app
            elevation="0"
            class="d-none d-md-block d-lg-block d-xl-block"
        >
            <div style="width: 1000px;"></div>
            <!-- <v-icon class="mt-1" style="transform: rotate(150deg);">mdi-timer-sand-empty</v-icon> -->
            <a href="/">
                <v-img style="cursor: pointer;" width="50px" src="../assets/Logo_gray.png"></v-img>
            </a>
			
            <div style="width: 20000px; color: red;"></div>
            <div
                class="btn"
                v-for="(item, index) in items" :key="index" :to="item.to">
                    <a :href="item.to" style="text-decoration: none; margin-left: 120px;">
                        <p class="medium list">{{ item.text }}</p>
                    </a>
                    
            </div>        
			<a href="#contact">
				<v-btn outlined class="medium mt-1" elevation="0">
					Contact
				</v-btn>
			</a>
            
            <div style="width: 1000px;"></div>
        </v-app-bar>
    
        <v-navigation-drawer 
        disable-resize-watcher
        v-model="drawer" 
        right
        class="mobile-drawer"
        app>
            <v-list style="height: 92%;">
				<div style="text-align: right;">
					<!-- <v-app-bar-nav-icon class="d-lg-none" id="drawer" @click="drawer = !drawer"></v-app-bar-nav-icon>  -->
					<v-icon large class="d-lg-none pr-3" id="drawer" @click="drawer = !drawer">mdi-close</v-icon>
					
				</div>
                
                <div class="btn" v-for="(item, index) in items" :key="index" :to="item.to" style="text-align: center;">

                    <a :href="item.to" style="text-decoration: none; display: block;">
                        
                        <p class="medium mobile-items">
                            <v-icon>{{ item.icon }}</v-icon>  
                            &nbsp;
                            {{ item.text }}
                        </p>
                    </a>
                    
                </div>
				<div style="text-align: center;">
					<a href="#contact">
						<v-btn outlined class="bold mt-1" elevation="0">
							Contact
						</v-btn>
					</a>
				</div>
				
            </v-list>
            
            <v-list-item>
                <!-- <v-list-item-icon>
                    <v-icon>mdi-account</v-icon>
                    </v-list-item-icon>
                <v-list-item-title>Login</v-list-item-title>  -->
            </v-list-item>
			
        </v-navigation-drawer>

		<!-- ///////////////////////////////////////////////////////////////////////////////////// -->

        <div>
            <!-- Homepage -->
            <div class="text-left" style="background-color: #e4f0fb;">
                <center>
                    <div style="position: relative; background-color: #efeee5;">
                        &nbsp;
                        <v-img data-aos="zoom-in" data-aos-easing="ease" data-aos-delay="100" data-aos-duration="1000" class="d-none d-sm-flex" style="position: relative; top: 0; left: 0;" src="../assets/Company_logo_c.png"></v-img>
                        <v-img class="d-flex d-sm-none" style="position: relative; top: 0; left: 0;" src="../assets/company_mobile.png"></v-img>
                        <!-- <v-img style="position: relative; top: 0; left: 0;" src="https://i0.wp.com/learn.onemonth.com/wp-content/uploads/2017/08/1-10.png?fit=845%2C503&ssl=1"></v-img> -->
                        <!-- <div style="position: absolute; top: 27%; left: 40%;">
                            <v-btn x-large>Explore Services</v-btn>
                            &nbsp;
                            <a href="">Talk to Us</a>
                        </div> -->
						<div class="d-block d-sm-none" style="">
							<v-btn class="bold" href="#solutions" style="text-decoration:none; color: white !important; background-color: #1b382a;">Explore Services</v-btn>
							&nbsp;
							<a href="#contact" class="medium" style="color: #125131; z-index: 2; position: relative;">Talk to Us</a>
						</div>

						<div data-aos="fade-up" data-aos-easing="ease" data-aos-delay="200" data-aos-duration="1000" class="d-none d-sm-block" style="margin-top: -30px;">
                            <!-- <h4 class="regular" style="margin-bottom: 20px;">``Providing <b>prime</b> results to your businesses``</h4> -->
                            <a href="#solutions">
                                <v-btn x-large class="bold" color="#125131" dark>Explore Services</v-btn>
                            </a>
							&nbsp;
							<a href="#contact" class="medium" style="color: #125131; z-index: 2; position: relative;">Talk to Us</a>
						</div>

                        <!-- Company -->
						<div id="company" style="height: 50px;"></div>

                        <div class="d-block d-sm-none" style="max-width: 800px; padding: 0 30px 0 30px; margin-top: 5%;">
                            <h1 class="bold pt-5">WHO WE ARE</h1>
                            &nbsp;
                            <p class="regular" style="margin: 0; font-size: 14px;">Teleprime Solutions Incorporated was established and registered on Jan 31, 2011, 
                                and situated in the business center of the Philippines. Its mission to provide the finest business solutions worldwide with utmost confidentiality, 
                                upholds the company’s standing in the industry.  As a top performing service provider in the country, we offer optimum business solutions here and around the globe. 
                                Built with the advanced technological system in telephony, internet and other medium of communication, Teleprime Solutions Inc has become the distinguished company in telemarketing, 
                                business processing, and comprehensive digital business servicing as it embodied its vision of becoming the prime provider of qualitative and quantitative business results at a very sensible cost.
                            </p>
                        </div>
                        <!-- pc -->
                        <div data-aos="fade-up" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1000" class="d-none d-sm-block" style="max-width: 800px; margin-top: 5%;">
                            <h1 class="bold">WHO WE ARE</h1>
                            &nbsp;
                            <p class="regular">Teleprime Solutions Incorporated was established and registered on Jan 31, 2011, 
                                and situated in the business center of the Philippines. Its mission to provide the finest business solutions worldwide with utmost confidentiality, 
                                upholds the company’s standing in the industry.  As a top performing service provider in the country, we offer optimum business solutions here and around the globe. 
                                Built with the advanced technological system in telephony, internet and other medium of communication, Teleprime Solutions Inc has become the distinguished company in telemarketing, 
                                business processing, and comprehensive digital business servicing as it embodied its vision of becoming the prime provider of qualitative and quantitative business results at a very sensible cost.
                            </p>
                        </div>
                        &nbsp;
                        <!-- mobile -->
                        <v-img class="d-flex d-sm-none" style="border-radius: 10px;" width="1000" height="300" src="../assets/company_banner.jpg"></v-img>
                        <v-btn class="medium d-flex d-sm-none" @click="organizationalStructure = true;" style="margin-top: 30px; color: #1B382A; border: #1B382A 1px solid;" elevation="0" block>Organizational Structure</v-btn>
                        <!-- pc -->
                        <v-parallax height="800" src="../assets/company_banner.jpg"></v-parallax>
                        <!-- <v-img class="d-none d-sm-block" style="border-radius: 10px;" width="900" height="600" src="../assets/company_banner.jpg"></v-img> -->
                        <v-btn class="medium d-none d-sm-block" @click="organizationalStructure = true;" style="margin-top: 30px; color: #1B382A; border: #1B382A 1px solid;" elevation="0" block>Organizational Structure</v-btn>
                        <!-- <v-img style="border-radius: 10px;" width="1000" height="500" src="../assets/Office_Picture.jpg"></v-img> -->
                        <!-- <v-img style="border-radius: 10px;" width="1000" height="500" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRweTCF-rdrKdxHw3y7nloAeDGXK9JJXehr4qjb76kh0e-9zyjW5sjslarnAdcqu36IF_Q&usqp=CAU"></v-img> -->
                        <div class="d-block d-sm-none" style="margin-top: 30px; padding-top: 2%; padding-bottom: 2%; justify-content: center; display: flex; background-color: #1B382A;">
                            <div>
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">
                                    <v-icon class="mb-2" x-large color="#D8EADA">mdi-arrow-up-drop-circle-outline</v-icon>100
                                </h1>
                                <p class="regular" style="color: #D8EADA; text-align: center; ">Employees</p>
                            </div>
                            <div>
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">SEC</h1>
                                <p class="regular" style="color: #D8EADA;">Registered 
                                    <br>January 31, 2011</p>
                                <p style="color: #D8EADA;"></p>
                            </div>
                            <div>
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">TM</h1>
                                <p class="regular" style="color: #D8EADA;">Registered No:
                                <br>4/2022/00527232</p>
                            </div>
                        </div> 
                        <!-- pc -->
                        <div class="d-none d-sm-flex" style="margin-top: 30px; padding-top: 2%; padding-bottom: 2%; justify-content: center; display: flex; background-color: #1B382A;">
                            <div data-aos="fade-up" data-aos-easing="ease" data-aos-delay="500" data-aos-duration="1200" >
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">
                                    <v-icon large color="white">mdi-arrow-up-drop-circle-outline</v-icon>100
                                </h1>
                                <p class="regular" style="color: #D8EADA; text-align: center; ">Employees</p>
                            </div>
                            <div class="ml-10" data-aos="fade-up" data-aos-easing="ease" data-aos-delay="600" data-aos-duration="1200">
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">SEC</h1>
                                <p class="regular" style="color: #D8EADA;">Registered 
                                    <br>January 31, 2011</p>
                                <p style="color: #D8EADA;"></p>
                            </div >
                            <div class="ml-10" data-aos="fade-up" data-aos-easing="ease" data-aos-delay="700" data-aos-duration="1400">
                                <h1 style="color: #D8EADA; font-family: 'Poppins', sans-serif; font-weight: 900; font-size: 50px;">TM</h1>
                                <p class="regular" style="color: #D8EADA;">Registered No:
                                    <br>4/2022/00527232</p>
                            </div>
                        </div> 

                        <!-- Solutions -->
						<div id="solutions" style="height: 50px;"></div>

                        <div style="margin-top: 60px;">
                            <div class="d-block d-sm-none" style="width: 90%; height:1100px; padding-top: 50px; border-radius: 5px; background-color: #D8EADA;">
                                <div style="width: 70%; background-color: ;">
                                    
                                    <div style="text-align: left;">
                                        <p class="medium" style="margin: 0;">what we do</p>
                                        <h1 class="bolder">Solutions</h1>
                                    </div>
                                    <div class="d-block" style="justify-content:center; display:flex; margin-bottom: 25px;">
                                        <div class="mt-5" @click="telemarketingDetails = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A; margin-right:30px;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Telemarketing</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/headset_mic_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                        <div class="mt-10" @click="advanceSolutions = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Advance Solutions</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/insights_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                        <div class="mt-10" @click="businessConsulting = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Business Consulting</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/question_answer_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                    </div>
                                    <div class="mt-10">
                                        <v-btn href="#contact" class="medium" style="border: 1px #1B382A solid; " large>Talk to Us</v-btn>	
                                    </div>		
                                </div>
                            </div>
                            <!-- pc solutions -->
                            <div class="d-none d-sm-block" style="width: 90%; height:500px; padding-top: 50px; border-radius: 5px; background-color: #D8EADA;">
                                <div data-aos="fade-right" data-aos-easing="ease-in-out" data-aos-delay="500" data-aos-duration="1400" style="width: 70%; background-color: ;">
                                    
                                    <div style="text-align: left; margin-bottom: 10px;">
                                        <p class="medium" style="margin: 0;">what we do</p>
                                        <h1 class="bolder">Solutions</h1>
                                    </div>
                                    <div style="justify-content:center; display:flex; margin-bottom: 25px;">
                                        <div class="telemarketing solutions" @click="telemarketingDetails = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A; margin-right:30px;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Telemarketing</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/headset_mic_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                        <div class="advanceSolutions solutions" @click="advanceSolutions = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Advance Solutions</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/insights_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                        <div class="businessConsulting solutions" @click="businessConsulting = true" style="border-radius: 5px; width: 250px; height:250px; background-color: #1B382A; margin-left:30px;">
                                            <div style="padding-top: 25px; padding-bottom: 25px;">
                                                <p class="regular" style="color: #D8EADA;">Business Consulting</p>
                                            </div>
                                            <div >
                                                <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/question_answer_black_24dp.svg"></v-img>
                                                <!-- <v-img style="margin-left: auto !important;" width="150" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                            </div>
                                        </div>
                                    </div>
                                    <div>
                                        <v-btn href="#contact" class="medium" style="border: 1px #1B382A solid; " large>Talk to Us</v-btn>	
                                    </div>		
                                </div>
								<!-- <div id="industries"></div> -->
                            </div>
                        </div>
						 
                        <!-- Industries -->
						<div id="industries" style="height: 50px;"></div>

                        <div style="margin-top: 60px;">
                            <div style="width: 90%; padding-top: 50px; padding-bottom: 40px; border-radius: 5px; background-color: #1B382A;">
                                <div class="d-block d-sm-none" style="width: 90% ; display: flex;">	
                                    <div style="text-align: left;">
                                        <p class="regular" style="margin: 0; color: #D8EADA;">we support</p>
                                        <h1 class="bold" style="color: #D8EADA;">Industries</h1>
                                    </div>
                                    <v-spacer/>
                                    <div class="mt-5" style="display: flex; overflow-x: scroll;">
                                        <div style="margin-left: auto !important;">
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Banking and Financial Services</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Healthcare</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Insurance</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-right: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Media</div>
                                        </div>
                                        <div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Government</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Retail and e-commerce</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Technology</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Telecom</div>
                                        </div>
                                        <div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-left: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Travel, Hospitality and Cargo</div>
                                        </div>
                                    </div>
                                </div>
                                <!-- pc -->
                                <div data-aos="fade-left" data-aos-easing="ease-in-out" data-aos-delay="500" data-aos-duration="1000" class="d-none d-sm-flex" style="width: 90% ; display: flex;">	
                                    <div style="text-align: left; margin-right: 30px;">
                                        <p class="regular" style="margin: 0; color: #D8EADA;">we support</p>
                                        <h1 class="bold" style="color: #D8EADA;">Industries</h1>
                                    </div>
                                    <v-spacer/>
                                    <div style="display: flex; overflow-x: scroll;">
                                        <div style="margin-left: auto !important;">
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Banking and Financial Services</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Healthcare</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px 0; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Insurance</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-right: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Media</div>
                                        </div>
                                        <div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin: 0 10px 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Government</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Retail and e-commerce</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Technology</div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Telecom</div>
                                        </div>
                                        <div>
                                            <div class="medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-left: 10px; border-radius: 5px; width: 250px; height: 100px; background-color: #D8EADA;">Travel, Hospitality and Cargo</div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <!-- Partners -->

                        <div style="margin-top: 50px;">
                            <p class="regular" style="margin: 0; color: #004323;">trusted by our partners</p>
                            <h1 class="bold" style="margin-bottom: 10px; color: #004323;">Partners</h1>
                            <!-- mobile -->
                            <v-card class="d-flex d-sm-flex d-lg-none" style="display: flex; flex-wrap: wrap;" elevation="0">
                                <v-card style="flex: 40% !important;" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/LAFLER_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/Pathland.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/shark_bottle.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/Trend_Artisans_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card href="https://nexwarekitchen.com/shop/" style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/NexWare_colored.png">
                                    </v-img>
                                </v-card>
                                <v-card href="https://www.comfortlivingph.com/" style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/Comfort_Living_ph_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card href="https://www.rcbc.com/" style="flex: 40% !important" elevation="0">
                                    <v-img aspect-ratio="2" contain src="../assets/partners/rcbc_colored.jpg">
                                    </v-img>
                                </v-card>
                            </v-card>

                            <!-- pc -->

                            <v-card class="d-none d-sm-none d-lg-flex" style="display: flex; flex-wrap: wrap;" elevation="0">
                                <v-card style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1000" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/LAFLER_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1200" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/Pathland.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1400" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/shark_bottle.jpg">
                                    </v-img>
                                </v-card>
                                <v-card style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1600" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/Trend_Artisans_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card href="https://nexwarekitchen.com/shop/" style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="1800" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/NexWare_colored.png">
                                    </v-img>
                                </v-card>
                                <v-card href="https://www.comfortlivingph.com/" style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="2000" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/Comfort_Living_ph_colored.jpg">
                                    </v-img>
                                </v-card>
                                <v-card href="https://www.rcbc.com/" style="flex: 1 0 21% !important;" elevation="0">
                                    <v-img data-aos="fade-down" data-aos-easing="ease" data-aos-delay="400" data-aos-duration="2200" class="imgPartners" aspect-ratio="2" contain src="../assets/partners/rcbc_colored.jpg">
                                    </v-img>
                                </v-card>
                            </v-card>
                            <div id="careers"></div>
                        </div>

                        <!-- careers -->

                        <div style="margin-top: 60px;">
                            <div class="d-block d-sm-none pb-5" style="display: flex;  background-color: white;">
                                <div>
                                    <v-img style="width: 100%; height: 200px" src="../assets/corporate.jpeg"></v-img>
                                    <!-- <v-img style="width: 100%; height: 200px" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                </div>
                                <!-- mobile -->
                                <div style="padding-left: 10%; padding-right: 10%; padding-top: 8%; padding-bottom: 5%;">
                                    <div style="text-align: left;">
                                        <p class="regular" style="margin: 0; color: #004323;">careers</p>
                                        <!-- <h1 class="bold" style="color: #004323;">Why Join Us?</h1> -->
                                        <h1 class="bold" style="color: #004323;">Join Our Team!</h1>
                                        <p class="regular mt-5" >we are looking for you</p>
                                        <!-- <p class="regular" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam ornare, orci vel egestas</p>
                                        <p class="medium" style="color: #004323;"><b>we are looking for you</b></p> -->
                                        <div @click="AccountSpecialistsDialog = true;" class="medium" style="background-color: #efeee5; font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; height: 100px; border: solid 1px #004323;">Account Specialists</div>
                                        <div @click="SalesVerifierDialog = true;" class="medium" style="background-color: #efeee5; font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; height: 100px; border: solid 1px #004323;">Sales Verifier</div>
                                        <!-- <v-btn elevation="3" class="regular mb-2" block style="color: #e4f0fb; background-color: #004323;" large>learn More
                                            <v-icon>mdi-information-outline</v-icon>
                                        </v-btn> -->
                                        <v-btn @click="ApplyNowDialog = true;" class="bold" style="color: #e4f0fb; background-color: #004323;" elevation="3" block large>Apply Now!</v-btn>
                                    </div>
                                </div>
                            </div>
                            <!-- pc -->
                            <div class="d-none d-sm-flex" style="display: flex;">
                                <div style="width: 50%;">
                                    <!-- <v-parallax style="width: 100%; height: 720px" src="../assets/corporate.jpeg"></v-parallax> -->
                                    <div class="parallax-img"></div>
                                    <!-- <v-img class="parallax-img" style="width: 100%; height: 720px" src="../assets/corporate.jpeg"></v-img> -->
                                    <!-- <v-img style="width: 100%; height: 720px" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                </div>
                                <div style="width: 50%; padding-left: 10%; padding-right: 5%; padding-top: 90px;">
                                    <div style="text-align: left;">
                                        <p class="regular" style="margin: 0; color: #004323;">careers</p>
                                        <!-- <h1 class="bold" style="color: #004323;">Why Join Us?</h1> -->
                                        <h1 class="bold" style="color: #004323;">Join Our Team!</h1>
                                        <!-- <p class="regular">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam ornare, orci vel egestas</p>
                                        <p class="medium" style="color: #004323;"><b>we are looking for you</b></p> -->
                                        <p class="regular mt-5">we are looking for you</p>
                                        <div @click="AccountSpecialistsDialog = true;" class="AccountSpecialistsDialog medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; height: 100px; border: solid 1px #004323;">Account Specialists</div>
                                        <div @click="SalesVerifierDialog = true;" class="SalesVerifierDialog medium" style="font-size: 20px; font-weight: bold; text-align: left; padding: 10px 0 0 10px; margin-bottom: 10px; border-radius: 5px; height: 100px; border: solid 1px #004323;">Sales Verifier</div>
                                        <!-- <v-btn class="regular mb-2" block style="color: #004323; border: #004323 1px solid;" large>learn More 
                                            <v-icon>mdi-information-outline</v-icon>
                                        </v-btn> -->
                                        <v-btn @click="ApplyNowDialog = true;" class="bold" block style="color: #e4f0fb; background-color: #004323;" large>Apply Now!</v-btn>
                                    </div>
                                </div>
                            </div>
							<div id="contact"></div>
                        </div>		

                        <!-- contact -->

                        <div style="margin-top: 40px;">
                            <div class="d-block d-sm-none pl-5 pr-5" style="display: flex;">
                                <div>
                                    <div style="text-align: left;">
                                        <p class="regular" style="margin: 0; color: #004323;">Get in touch</p>
                                        <h1 class="bold" style="color: #004323; margin-bottom: 10px;">Our Location</h1>
                                        <v-row style="flex-wrap: nowrap !important;">
                                            <v-icon class="ml-3">mdi-map-marker</v-icon>&nbsp;
                                            <p class="regular" style="margin: 10px 0 3px 0; flex-wrap; padding-right: 5%;">Business Address: Unit 3102A East Tower Philippine Stock Exchange Centre, Exchange
                                            Rd., Ortigas Center, Pasig</p>
                                        </v-row>
                                        <v-row style="flex-wrap: none;">
                                            <v-icon class="ml-3">mdi-phone</v-icon>&nbsp;
                                            <p class="regular" style="margin: 5px 0 3px 0;">8575-1888</p>
                                        </v-row>
                                        <v-row style="flex-wrap: none;">
                                            <v-icon class="ml-3">mdi-email</v-icon>&nbsp;
                                            <p class="regular" style="margin: 5px 0 3px 0;">info@teleprimesolutions.com</p>
                                        </v-row>
                                        &nbsp;
                                        <iframe width="100%" height="300" style="border:1px solid black; margin-top: 3%;" allowfullscreen="" loading="lazy" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3246.9445289800565!2d121.06305499950754!3d14.582570617708418!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397c813fb0cc52d%3A0xc41dcbacee31c1fb!2sTeleprime%20Solutions%20Incorporated!5e0!3m2!1sen!2sph!4v1687603969161!5m2!1sen!2sph" referrerpolicy="no-referrer-when-downgrade"></iframe>
                                    </div>
                                    
                                    <!-- <v-img style="width: 100%; height: 720px" src="../assets/corporate.jpeg"></v-img> -->
                                </div>
                                <div style="padding-left: 10%; padding-right: 10%; padding-top: 5%; padding-bottom: 5%;">
                                    <div style="text-align: left;">
                                        <h1 class="bold" style="color: #004323;">Have a Question?</h1>
                                        <h2 class="medium" style="color: #004323;">Let's Have a Talk!</h2>
                                        <v-text-field class="mt-5 mb-2" outlined label="Full Name" hide-details style="background-color: white;"></v-text-field>
                                        <v-text-field class="mb-2" outlined label="Email" hide-details style="background-color: white;"></v-text-field>
                                        <v-text-field class="mb-2" outlined label="Phone" hide-details style="background-color: white;"></v-text-field>
                                        <v-textarea class="mb-2" outlined label="Message" hide-details style="background-color: white;"></v-textarea>
                                        <v-btn class="bold" large block style="background-color: #004323; color: white;">Submit</v-btn>
                                    </div>
                                </div>
                            </div>
                            <!-- pc -->
                            <div class="d-none d-sm-flex" style="display: flex;">
                                <div style="width: 50%; padding-left: 10%; padding-right: 5%; padding-top: 3%;">
                                    <div style="text-align: left;">
                                        <h1 class="bold" style="color: #004323;">Have a Question?</h1>
                                        <h2 class="medium" style="color: #004323;">Let's Have a Talk!</h2>
                                        <v-text-field class="mt-5 mb-2" outlined label="Full Name" hide-details style="background-color: white;"></v-text-field>
                                        <v-text-field class="mb-2" outlined label="Email" hide-details style="background-color: white;"></v-text-field>
                                        <v-text-field class="mb-2" outlined label="Phone" hide-details style="background-color: white;"></v-text-field>
                                        <v-textarea class="mb-2" outlined label="Message" hide-details style="background-color: white;"></v-textarea>
                                        <v-btn class="bold" large block style="background-color: #004323; color: white;">Submit</v-btn>
                                    </div>
                                </div>
                                <div style="width: 50%;">
                                    <div style="text-align: left;">
                                        <p class="regular" style="margin: 0; color: #004323;">Get in touch</p>
                                        <h1 class="bold" style="color: #004323;">Our Location</h1>
                                        <v-row style="flex-wrap: nowrap !important;">
                                            <v-icon class="ml-3 mr-3" large>mdi-map-marker</v-icon>
                                            <p class="regular" style="margin: 10px 0 3px 0; flex-wrap; padding-right: 20%;">Business Address: Unit 3102A East Tower Philippine Stock Exchange Centre, Exchange
                                            Rd., Ortigas Center, Pasig</p>
                                        </v-row>
                                        <v-row style="flex-wrap: none;">
                                            <v-icon class="ml-3 mr-3" large>mdi-phone</v-icon>
                                            <p class="regular" style="margin: 5px 0 3px 0;">8575-1888</p>
                                        </v-row>
                                        <v-row style="flex-wrap: none;">
                                            <v-icon class="ml-3 mr-3" large >mdi-email</v-icon>
                                            <p class="regular" style="margin: 5px 0 3px 0;">info@teleprimesolutions.com</p>
                                        </v-row>
                                        <iframe width="500" height="400" style="border:1px solid black; margin-top: 3%;" allowfullscreen="" loading="lazy" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3246.9445289800565!2d121.06305499950754!3d14.582570617708418!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397c813fb0cc52d%3A0xc41dcbacee31c1fb!2sTeleprime%20Solutions%20Incorporated!5e0!3m2!1sen!2sph!4v1687603969161!5m2!1sen!2sph" referrerpolicy="no-referrer-when-downgrade"></iframe>
                                    </div>
                                    
                                    <!-- <v-img style="width: 100%; height: 720px" src="../assets/corporate.jpeg"></v-img> -->
                                </div>
                            </div>
                        </div>	

                        <!-- footer -->
                        
                        <div class="d-block d-sm-block d-md-none" style="margin-top: 30px; padding-top: 20px; background-color: #00180D">
                            <!-- <v-row> -->
                                <v-col>
                                    <v-img width="500" src="../assets/tele_white.png"></v-img>
                                    <!-- <v-img width="200" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                </v-col>
                                <!-- <v-divider></v-divider> -->
                                <v-col style="text-align: center; padding-right: 4%; padding-top: 1%; padding-bottom: 10%;">
                                        <p class="medium" style="color: white;">CONNECT WITH US:</p>
                                        <v-icon class="mr-5" color="white">mdi-facebook</v-icon>
                                        <v-icon class="mr-5" color="white">mdi-instagram</v-icon>
                                        <v-icon class="mr-5" color="white">mdi-twitter</v-icon>
                                        <v-icon color="white">mdi-wechat</v-icon>
                                        
                                    <div style="display: flex; justify-content: center; margin-top: 10%;">
                                        <a style="text-decoration: none;" href="#company">
                                            <p id="company" class="regular mr-5" style="color: white;">Company</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#solutions">
                                            <p id="solutions" class="regular mr-5" style="color: white;">Solutions</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#industries">
                                            <p id="industries" class="regular mr-5" style="color: white;">Industries</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#careers">
                                            <p id="careers" class="regular" style="color: white;">Careers</p>    
                                        </a>
                                    </div>
                                </v-col>
                            <!-- </v-row> -->
                        </div>	
                        <!-- pc -->
                        <div class="d-none d-sm-none d-md-block" style="margin-top: 50px;  height: 200px; background-color: #00180D;">
                            <v-row>
                                <v-col>
                                    <v-img class="pt-1" width="430" src="../assets/tele_white.png"></v-img>
                                    <!-- <v-img width="200" src="https://developers.google.com/static/maps/documentation/streetview/images/error-image-generic.png"></v-img> -->
                                </v-col>
                                <v-divider></v-divider>
                                <v-col style="text-align: right; padding-right: 4%; margin-top: 25px; background-color: #00180D;">
                                        <p class="medium" style="color: white;">CONNECT WITH US:</p>
                                        <v-icon color="white">mdi-facebook</v-icon>
                                        &nbsp;
                                        <v-icon color="white">mdi-instagram</v-icon>
                                        &nbsp;
                                        <v-icon color="white">mdi-twitter</v-icon>
                                        &nbsp;
                                        <v-icon color="white">mdi-wechat</v-icon>
                                        
                                    <div style="display: flex; justify-content: end; margin-top: 20px;">
                                        <!-- <p id="company" class="regular mr-5" style="color: white;">Company</p>
                                        <p id="solutions" class="regular mr-5" style="color: white;">Solutions</p>
                                        <p id="industries" class="regular mr-5" style="color: white;">Industries</p>
                                        <p id="careers" class="regular" style="color: white;">Careers</p> -->
                                        <a style="text-decoration: none;" href="#company">
                                            <p id="company" class="regular mr-5" style="color: white;">Company</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#solutions">
                                            <p id="solutions" class="regular mr-5" style="color: white;">Solutions</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#industries">
                                            <p id="industries" class="regular mr-5" style="color: white;">Industries</p>
                                        </a>
                                        <a style="text-decoration: none;" href="#careers">
                                            <p id="careers" class="regular" style="color: white;">Careers</p>    
                                        </a>
                                    </div>
                                </v-col>
                            </v-row>
                        </div>	
                    </div>
                </center>
            </div>
        </div>

        <v-dialog
            v-model="telemarketingDetails"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                    Telemarketing
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                A business solution that offers, but not limited to inbound, outbound, lead generation and sales to clients that entails marketing research, telesales, surveying. Our aim is to address the clients’ need-based selling, market research, and other telemarketing activities. Teleprime Solutions Inc is determined to deliver excellent solutions according to the clients’ business objectives and goals.
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="#1b382a"
                    text
                    @click="telemarketingDetails = false"
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                    Close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>

        <v-dialog
            v-model="businessConsulting"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Business Consulting
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                Our business consulting services focus on the enterprise most concerning issues and opportunities: strategy, marketing, organization, operations, technology, transformation, digital, advanced analytics, corporate finance, mergers & acquisitions, and sustainability across all industries worldwide. We deliver functional solutions, faster and more adaptable client-focused systems to achieve business extraordinary results. Teleprime Solutions Inc guarantees that services are made not only to deliver, but also to give prime results that exceed the clients’ expectations.
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="#1b382a"
                    text
                    @click="businessConsulting = false"
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                    Close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>

        <v-dialog
            v-model="advanceSolutions"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Advance Solutions
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                Teleprime Solutions Inc understands the enterprise needs amidst the fast-changing economic situation worldwide. Our aim is to help your business operate more efficiently. Teleprime Solutions Inc will give you boundless assistance from procurement of location, construction, business license and permits acquisition, 9(g) working visa for alien employees, trademark registration, and many more. With technical and intellectual expertise, Teleprime Solutions Inc promises to bring solutions and strategic alignment to clients’ business objectives and needs.
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="#1b382a"
                    text
                    @click="advanceSolutions = false"
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                    Close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>

        <!-- <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/question_answer_black_24dp.svg"></v-img>
        <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/insights_black_24dp.svg"></v-img>
        <v-img style="margin-left: auto !important;" width="150" src="../assets/icons/headset_mic_black_24dp.svg"></v-img> -->

        <v-dialog
            v-model="AccountSpecialistsDialog"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Account Specialists
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                Responsible for selling some products or service to the customers through telephonic calls. 
                The outbound call center executives are not only assigned the task of selling products or services, 
                but they may be required for promotion of a product, taking feedback from customers, 
                or for providing some information to people over telephone.
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="#1b382a"
                    text
                    @click="AccountSpecialistsDialog = false"
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                    Close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>

        <v-dialog
            v-model="SalesVerifierDialog"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Sales Verifier
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                Effectively validate sales, activation, etc. 
                for accuracy and reports discrepancies in a timely and appropriate manner.
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                    color="#1b382a"
                    text
                    @click="SalesVerifierDialog = false"
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                    Close
                </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>

        <!-- /////////////////////// Apply now ////////////////////// -->

        <v-dialog
            v-model="ApplyNowDialog"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Form
                <v-spacer/>
                <v-btn
                    color="#d8eada"
                    text
                    @click="ApplyNowDialog = false"
                    icon
                    large
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                </v-btn>
                </v-card-title>
                
                &nbsp;

                <v-card-text class="regular" style="font-size: 16px;">
                <div style="text-align: left;">
                    <v-select
                        v-model="career"
                        :rules="[() => !!career || 'This field is required']"
                        class="mt-2 mb-2"  
                        hide-details 
                        style="background-color: white;"
                        :items="careers"
                        label="You are applying for?"
                        outlined
                    ></v-select>
                    <v-text-field 
                        v-model="FullName"
                        :rules="[() => !!FullName || 'This field is required']"
                        class="mb-2" outlined label="Full Name" hide-details="auto" style="background-color: white;"></v-text-field>
                    <v-text-field 
                        prepend-inner-icon="mdi-email"
                        placeholder="Email"
                        :rules="[rules.required, rules.email]"
                        class="mb-2" outlined label="Email" hide-details="auto" style="background-color: white;"></v-text-field>
                    <v-text-field 
                        v-model="Phone"
                        :rules="[rules.required, rules.numberOnly]"
                        class="mb-2" outlined label="Phone" hide-details="auto" style="background-color: white;"></v-text-field>
                    <v-textarea 
                        v-model="Message"
                        :rules="[() => !!Message || 'This field is required']"
                        class="mb-2" outlined label="Message" hide-details="auto" style="background-color: white;"></v-textarea>
                    <v-btn class="bold" large block style="background-color: #004323; color: white;">Submit</v-btn>
                </div>
                </v-card-text>
            </v-card>
        </v-dialog>

        <v-dialog
            v-model="organizationalStructure"
            width="500"
            persistent
            >

            <v-card>
                <v-card-title class="bold" style="background-color: #1b382a; color: #d8eada;">
                Organizational <br>Structure
                <v-spacer/>
                <v-btn
                    color="#d8eada"
                    text
                    @click="organizationalStructure = false"
                    icon
                    large
                >
                    <v-icon>
                        mdi-close
                    </v-icon>
                </v-btn>
                </v-card-title>
                
                &nbsp;

                <v-card class="d-none d-sm-flex">
                    <v-img width="600" height="800" src="../assets/Organizational_Chart.png"></v-img>
                </v-card>
                <v-card class="d-flex d-sm-none">
                    <v-img width="500" height="650" src="../assets/Organizational_Chart.png"></v-img>
                </v-card>
            </v-card>
        </v-dialog>
    </v-app>
  	
</template>

<script>
import AOS from 'aos';
//Initialize manually in every divs
AOS.init();
  export default {
    name: 'TeleprimeSolutionsInc',

    data: () => ({
        organizationalStructure: false,
        SalesVerifierDialog: false,
        AccountSpecialistsDialog: false,
        telemarketingDetails: false,
        ApplyNowDialog: false,
        careers: ['Account Specialists','Sales Verifier'],
        career: '',
        FullName: '',
        Phone: '',
        Message: '',
        rules: {
            required: value => !!value || 'Required.',
            counter: value => value.length <= 20 || 'Max 20 characters',
            email: value => {
                const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
                return pattern.test(value) || 'Invalid e-mail.'
            },   
            numberOnly: value => {
                return /^\d*\+?\d*$/.test(value) || 'Invalid Phone Number';
            }
        },
        businessConsulting: false,
        advanceSolutions: false,
		drawer: false,
		items:[
			{text:'Home', icon:'mdi-home', to:'/'},
			{text:'Company', icon:'mdi-archive-outline', to:'#company'},
			{text:'Solutions', icon:'mdi-tools', to:'#solutions'},
			{text:'Industries', icon:'mdi-information-outline', to:'#industries'},
			{text:'Careers', icon:'mdi-phone', to:'#careers'},
		]
    }),
  }
</script>

<style>
.v-application .ma-2{
	margin: 0 !important;
}
/* padding && margin errors are here */
.v-main{ 
	padding: 50px 0px 0px !important;
}
.btn {
	border-radius: 5px;
	font-family: 'Segoe UI';
	font-weight: bold;
}
.v-application a{
	color: #3b3e42 !important;
}
.list:hover{
	color: green;
}
.mobile-drawer{
	width: 100% !important;
}
.v-toolbar__content{
	width: 100% !important;
	justify-content: space-between !important;
}
.mobile-items{
	padding-top: 20px; 
	padding-bottom: 20px;
	margin: 0 !important;
}
.mobile-items:hover{
	background-color: #afe2ff;
}

html {
  scroll-behavior: smooth;
}
.canvas{
	margin-left: 300px;
	margin-right: 300px;
}

.regular{
    font-family: 'Poppins', sans-serif !important; 
    font-weight: 400 !important;
}

.medium{
    font-family: 'Poppins', sans-serif !important; 
    font-weight: 500 !important;
}

.semiBold{
    font-family: 'Poppins', sans-serif !important; 
    font-weight: 600 !important;
}

.bold{
    font-family: 'Poppins', sans-serif !important; 
    font-weight: 700 !important;
}

.bolder{
	font-family: 'Poppins', sans-serif !important; 
    font-weight: 800 !important;
}

.boldest{
	font-family: 'Poppins', sans-serif !important; 
    font-weight: 900 !important;
}

.solutions:hover{
    cursor: pointer;
}

.imgPartners {
    filter: grayscale(100%);
    -webkit-filter: grayscale(100%);
}

.imgPartners:hover {
    filter: none;
    -webkit-filter: grayscale(0);
    cursor: pointer;
}   

.telemarketing:hover{
    box-shadow: 6px 7px 0px 0px rgba(0,0,0,0.3);
}

.advanceSolutions:hover{
    box-shadow: 6px 7px 0px 0px rgba(0,0,0,0.3);
}

.businessConsulting:hover{
    box-shadow: 6px 7px 0px 0px rgba(0,0,0,0.3);
}

.AccountSpecialistsDialog:hover{
    color: rgb(216, 234, 218);
    background-color:rgb(27, 56, 42);
    cursor: pointer;
}

.SalesVerifierDialog:hover{
    color: rgb(216, 234, 218);
    background-color: rgb(27, 56, 42);
    cursor: pointer;
}

.parallax-img{
    /* The image used */
    background-image: url("../assets/corporate.jpeg");

    /* Set a specific height */
    min-height: 500px;
    width: 100%; 
    height: 720px;

    /* Create the parallax scrolling effect */
    background-attachment: fixed;
    /* background-position: center; */
    background-repeat: no-repeat;
    /* background-size: cover; */
}

@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
</style>
