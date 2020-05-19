<template>
  <div class="developer-card">
    <link rel="stylesheet" href="main.css" />
    <div class="deleoper-card-avatar-wrapper">
      <div class="deleoper-card-avatar-image">
        <img src="@/assets/image_profile.png" />
      </div>

      <div class="rate-wrapper">
        <div class="ratestars">
          <svg width="110" height="13" viewBox="0 0 110 13" fill="none" xmlns="http://www.w3.org/2000/svg">
<mask id="mask0" mask-type="alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="110" height="13">
<path d="M6.99993 0L8.57152 4.83688H13.6573L9.54282 7.82624L11.1144 12.6631L6.99993 9.67376L2.88543 12.6631L4.45703 7.82624L0.342529 4.83688H5.42833L6.99993 0Z" fill="white"/>
<path d="M30.9999 0L32.5715 4.83688H37.6573L33.5428 7.82624L35.1144 12.6631L30.9999 9.67376L26.8854 12.6631L28.457 7.82624L24.3425 4.83688H29.4283L30.9999 0Z" fill="white"/>
<path d="M54.9999 0L56.5715 4.83688H61.6573L57.5428 7.82624L59.1144 12.6631L54.9999 9.67376L50.8854 12.6631L52.457 7.82624L48.3425 4.83688H53.4283L54.9999 0Z" fill="white"/>
<path d="M78.9999 0L80.5715 4.83688H85.6573L81.5428 7.82624L83.1144 12.6631L78.9999 9.67376L74.8854 12.6631L76.457 7.82624L72.3425 4.83688H77.4283L78.9999 0Z" fill="white"/>
<path d="M103 0L104.572 4.83688H109.657L105.543 7.82624L107.114 12.6631L103 9.67376L98.8854 12.6631L100.457 7.82624L96.3425 4.83688H101.428L103 0Z" fill="white"/>
</mask>
<g mask="url(#mask0)">
<rect x="-2" y="-2" width="72" height="18" rx="2" fill="url(#paint0_linear)"/>
</g>
<defs>
<linearGradient id="paint0_linear" x1="-6.67999" y1="-36.02" x2="47.86" y2="44.62" gradientUnits="userSpaceOnUse">
<stop stop-color="#FF9C06"/>
<stop offset="1" stop-color="#6C8DFF"/>
</linearGradient>
</defs>
</svg>
<div class="rate-two">
<svg width="110" height="14" viewBox="0 0 110 14" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M79 0L80.5716 4.83688H85.6574L81.5429 7.82624L83.1145 12.6631L79 9.67376L74.8855 12.6631L76.4571 7.82624L72.3426 4.83688H77.4284L79 0Z" fill="white" fill-opacity="0.2"/>
<path d="M103 0L104.572 4.83688H109.657L105.543 7.82624L107.114 12.6631L103 9.67376L98.8855 12.6631L100.457 7.82624L96.3426 4.83688H101.428L103 0Z" fill="white" fill-opacity="0.2"/>
</svg>
</div>
        </div>
      </div>


    </div>
    <div class="developer-card-main-info-wrapper">
      <div class="developer-card-main-info">
        <div class="developer-card-main-info-left">
          <div class="developer-card-developer-name">
            {{ developerName }}
          </div>
          <div class="years-old">
            <div class="years-old-header developer-card-header">
              <p>Возраст и стаж: </p>
            </div>
            <div class="years-old-text developer-card-text">
              <span>{{ developerYears }}</span>
            </div>
          </div>

          <div class="activity">
            <div class="activity-header developer-card-header">
              <p>Вид деятельности: </p>
            </div>
            <div class="activity-old-text developer-card-text">
              <span>{{ developerActivity }}</span>
            </div>
          </div>

          <div class="direction">
            <div class="direction-header developer-card-header">
              <p>Направление: </p>
            </div>
            <div class="direction-old-text developer-card-text">
              <span>{{ developerDirection }}</span>
            </div>
          </div>
          <div class="tech-skills">
            <div
              class="developer-card-tech-special"
              v-for="skill in special"
              :key="skill"
            >
              <span>{{ skill }}</span>
            </div>
          </div>
        </div>

        <div class="qual">
          <p>Квалификация:</p>
          <div class="dev-qual">
            <span>{{ qualification }}</span>
          </div>
        </div>

        
      </div>
    </div>
    <div class="developer-card-payment-info-wrapper">
      <div class="hour">
        <p>Ставка в час:</p>
        <div class="PerHour">
          <span>{{ developerHour }}</span>
        </div>
      </div>
      <div class="developer-card-wrapper">
        <div class="inn">
          <p>ИНН:</p>
          <div class="dev-inn">
            <span>{{ developerInn }}</span>
          </div>
        </div>

        <div class="dev-ep">
          <span>{{ developerEP }}</span>
        </div>

        <div class="system">
          <p>Система налогооблажения:</p>
        </div>
        <div class="dev-system">
          <span>{{ developerSystem }}</span>
        </div>
      </div>
    </div>
    <div></div>

    <div class="developer-card-tech-skills">
      <div
        class="developer-card-tech-skills-skill"
        v-for="skill in techStack"
        :key="skill"
      >
        {{ skill }}
      </div>
</div>
<div class="wrapper-button">
          <div class="gradient">
            <div class="button-gradient">
              <button class="button">Нанять</button>
            </div>
          </div>
        </div>

      <div class="wrap-flag">
      <div class="flag-1">
        <div class="flag">
            <a href="#"><img src="@/assets/flag.png" /></a>
        </div>
        </div>
        <div class="rectangle_flag">
          <a href="#"><img src="@/assets/rectangle_flag.png"/></a>
        </div>
        </div>


  </div>

</template>
<script>
export default {
  name: "DeveloperCard",
  props: {
    developerName: String,
    developerSurname: String,
    techStack: Array,
    developerActivity: String,
    special: Array,
    qualification: String,
    developerDirection: String,
    developerYears: String,
    developerHour: String,
    developerEP: String,
    developerInn: String,
    developerSystem: String
  }
};

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');

.dev-ep {
float: right;
margin-right: 25px;
color: rgba(255, 255, 255, 0.4);
}
.rate-two{
  margin-top: -20px;
  
}
.rate-wrapper{
margin-left: 840px;
margin-top: -80px;
}
.developer-card-tech-skills {
  margin-top: 270px;
  margin-left: 127px;
  position: absolute;
}
.developer-card-wrapper {
  float: right;
  margin-left: 50px;
}
.flag{
  margin-top: -38px;
    float: right;
    position: center;
  margin-right: 179px;
}
.rectangle_flag{
   margin-top: -45px;
  float: right;
  margin-right: 170px;
}

.developer-card-tech-skills-skill {
  margin: 5px;
  display: inline-block;
  padding-top: 80%;
  color: rgba(255, 255, 255, 0.4);
  padding: 5px;

  font-size: 14px;

  background: #3a3a3a;
}
.deleoper-card-avatar-image {
  margin-left: 20px;
  margin-top: 20px;
}
.deleoper-card-avatar-wrapper {
  width: 10%;
  height: 100%;

  float: left;
}
.developer-card-main-info-wrapper {
  width: 70%;

  height: 100%;
  float: left;
}
.developer-card-developer-name {
  font-size: 24px;
  margin-top: 20px;
}

.developer-card-payment-info-wrapper {
  width: 20%;
  height: 100%;
  float: right;
  background-color: #2e2e2e;
}
.developer-card-main-info-left {
  float: left;
  color: #fff;
}
.developer-card-main-info-left-right {
  float: left;
  margin-left: 250px;
}
.developer-card-header {
  display: inline-block;
  color: rgba(255, 255, 255, 0.4);
}

.developer-card-text {
  display: inline-block;
  color: #fff;
}
</style>
<style scoped lang="scss">
.developer-card {
  background: #282828;
  height: 317px;
  width: 1360px;
  border: 1px solid #2121;
  border-radius: 1px;
  margin: 20px;
}
.qual {
  display: inline-block;
  color: grey;
    font-family: 'SF UI Display', sans-serif;

  margin-top: 40px;
  font-style: normal;
  margin-left: 250px;
}
.dev-qual {
  color: #fff;
  margin-left: 135px;
  margin-top: -34px;
}
.inn {
  color: rgba(255, 255, 255, 0.4);
  margin-left: 100px;
  margin-top: 40px;
}
.dev-inn {
  margin-top: -35px;
  color: rgba(255, 255, 255, 0.4);
  float: right;
  margin-right: 25px;
  font-weight: 300;
  font-size: 14px;
  line-height: 20px;
}
.hour {
  color: rgba(255, 255, 255, 0.4);
  font-size: 12px;
}
.PerHour {
  color: #fff;
  font-size: 24px;
}

.hour {
  margin-top: 70px;
  margin-left: 60px;
  font-family: 'SF UI Display', sans-serif;

}

.PerHour {
  margin-left: 110px;
  font-family: 'SF UI Display', sans-serif;
  margin-top: -35px;
}
.system {
  color: rgba(255, 255, 255, 0.4);
  display: inline-block;
  font-weight: 300;
font-size: 14px;
    font-family: 'SF UI Display', sans-serif;

line-height: 20px;
}
.dev-system {
  color: rgba(255, 255, 255, 0.4);
  margin-left: 200px;
  margin-top: -32px;
  margin-right: 25px;
  
}

.developer-card-tech-special {
  float: left;
  margin-right: 10px;
}
.developer-card-tech-special::after {
  content: "•";
  margin-left: 10px;
}
.developer-card-tech-skill::after {
  margin-left: 10px;
}
.activity {
  margin-top: -12px;
  font-weight: 10;
font-size: 14px; 
font-family: 'SF UI Display', sans-serif;

line-height: 20px;
}
.direction {
  margin-top: -12px;
  font-weight: 300;
font-size: 14px;
    font-family: 'SF UI Display', sans-serif;

line-height: 20px;
}
.qual{
  position: absolute;
margin-top: 35px;
margin-left: -300px;
font-weight: 300;
    font-family: 'SF UI Display', sans-serif;

font-size: 14px;
line-height: 20px;
}
.developer-card-tech-skills{
  margin-top: 240px;
}
.button{
  width: 120px;
  height: 32px;
  float: right;
  font-family: 'SF UI Display', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  margin-right: 25px;
  margin-top: -45px;
  color: #fff;
  border-radius: 2px;
  background: linear-gradient(144.19deg, #FF9C06 -55.75%, #6C8DFF 120.46%);
}
.years-old{
  font-weight: 300;
 font-size: 14px;
 line-height: 20px;
}

</style>
