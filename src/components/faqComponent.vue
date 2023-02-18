<template>
	<div class="ilustartionContainer">
		<img
			class="bg-pattern-desktop"
			alt="background for desktop"
			src="..//images/bg-pattern-desktop.svg" />
		<img
			class="illustration-woman-online-desktop"
			alt="woman front of screen"
			src="../images/illustration-woman-online-desktop.svg" />
		<img
			class="illustration-woman-online-mobile"
			alt="woman front of screen"
			src="../images/illustration-woman-online-mobile.svg" />
	</div>
	<div class="faqContainer">
		<h1>FAQ</h1>
		<ul class="faqList">
			<li>
				<p class="questionText" @click="readButton($event)" id="1" :class="{'clicked':clickedButton==1}">
					How many team members can I invite?
					<button class="arrowButton">
						<img
							class="arrow-down-icon"
							:class="{'rotateButton':clickedButton==1}"
							alt="Arrow down icon"
							src="../images/icon-arrow-down.svg" />
					</button>
				</p>

				<p class="answer" :class="{'answerActive':clickedButton==1}">
					You can invite up to 2 additional users on the Free plan. There is no
					limit on team members for the Premium plan.
				</p>
			</li>
			<li>
				<p class="questionText" @click="readButton($event)" id="2" :class="{'clicked':clickedButton==2}">
					What is the maximum file upload size?<button class="arrowButton">
						<img
							class="arrow-down-icon"
							:class="{'rotateButton':clickedButton==2}"
							alt="Arrow down icon"
							src="../images/icon-arrow-down.svg" />
					</button>
				</p>

				<p class="answer" :class="{'answerActive':clickedButton==2}">
					No more than 2GB. All files in your account must fit your allotted
					storage space.
				</p>
			</li>
			<li>
				<p class="questionText" @click="readButton($event)" id="3" :class="{'clicked':clickedButton==3}">
					How do I reset my password?
					<button class="arrowButton">
						<img
							class="arrow-down-icon"
							:class="{'rotateButton':clickedButton==3}"
							alt="Arrow down icon"
							src="../images/icon-arrow-down.svg" />
					</button>
				</p>

				<p class="answer" :class="{'answerActive':clickedButton==3}">
					Click “Forgot password” from the login page or “Change password” from
					your profile page. A reset link will be emailed to you.
				</p>
			</li>
			<li>
				<p class="questionText" @click="readButton($event)" id="4" :class="{'clicked':clickedButton==4}">
					Can I cancel my subscription?<button class="arrowButton">
						<img
							class="arrow-down-icon"
							:class="{'rotateButton':clickedButton==4}"
							alt="Arrow down icon"
							src="../images/icon-arrow-down.svg" />
					</button>
				</p>

				<p class="answer" :class="{'answerActive':clickedButton==4}">
					Yes! Send us a message and we’ll process your request no questions
					asked.
				</p>
			</li>
			<li>
				<p class="questionText" @click="readButton($event)" id="5" :class="{'clicked':clickedButton==5}">
					Do you provide additional support?<button class="arrowButton">
						<img
							class="arrow-down-icon"
							:class="{'rotateButton':clickedButton==5}"
							alt="Arrow down icon"
							src="../images/icon-arrow-down.svg" />
					</button>
				</p>

				<p class="answer" :class="{'answerActive':clickedButton==5}">
					Chat and email support is available 24/7. Phone lines are open during
					normal business hours
				</p>
			</li>
			.
		</ul>
	</div>
	<img
		class="illustration-box-desktop"
		ale="box wit@"
		src="../images/illustration-box-desktop.svg " />
</template>

<script>
import { ref } from "vue";
export default {
	name: "faqComponent",
	setup() {
		let clickedButton = ref(0);
		function readButton(e) {
			if(clickedButton.value!=e.currentTarget.id){
			clickedButton.value=e.currentTarget.id;
			}
			else{
				clickedButton.value =0;
			}
		}

		return {
			readButton,
			clickedButton,
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
@import url(./style.css);
@import url(./mobile.css);
</style>
