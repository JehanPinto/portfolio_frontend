<template>
  <div>
    <h1>{{name}}</h1>
    <h2>Projects</h2>
    <div v-if="pending1">Loading...</div>
    <ul>
      <li v-for="project in projects" :key="project.name">
        <h2>{{project.name}}</h2>
        <p>{{project.description}}</p>
      </li>
    </ul>
  </div>
  <div>
    <h2>Blogs</h2>
    <div v-if="pending2">Loading...</div>
    <ul>
      <li v-for="blog in blogs" :key="blog.title">
        <h2>{{blog.title}}</h2>
        <p>{{blog.content}}</p>
      </li>
    </ul>
  </div>
  <section class=" WHY-CHOOSE-US WCU-s w-100 py-2 py-lg-5">
        <div class="container ">
            <div class="d-flex flex-column align-items-center mb-4">
                <div class="col-6 col-md-4 col-lg-3 d-flex flex-column align-items-center">
                    <span class="alg-text-blue mt-1 fw-bolder alg-text-h2 pb-1">bootsrap testing</span>
                    <div class="alg-line1 alg-bg-blue d-flex align-self-center"></div>
                    <div class="alg-line2 alg-bg-blue d-flex align-self-center"></div>
                </div>
            </div>
            <div class="feat bg-gray pt-5 pb-5">
    <div class="container">
      <div class="row">
        <div class="section-head col-sm-12">
          
          <p>When you choose us, you're tapping into a decade of expertise in automotive parts procurement. Our seasoned team understands the intricacies of the industry, ensuring seamless transactions and top-notch customer service. From navigating the complexities of online orders to optimizing your experience with cutting-edge SEO and social media strategies, 
            we're dedicated to delivering unparalleled support every step of the way.</p>
        </div>
        <div class="col-lg-4 col-sm-6">
          <div class="item"> <span class="icon feature_box_col_one"><i class="fa fa-globe"></i></span>
            <h6>Nationwide Accessibility</h6>
            <p> Say goodbye to the hassle of finding specific parts locally. With our nationwide delivery service, you can order from the
                 comfort of your home and have the parts delivered directly to your doorstep, regardless of your location.</p>
          </div>
        </div>
        <div class="col-lg-4 col-sm-6">
          <div class="item"> <span class="icon feature_box_col_two"><i class="fa fa-anchor"></i></span>
            <h6>Wide Range of Parts</h6>
            <p>  Explore our extensive inventory catering to every make and model, ensuring you find the right part for your vehicle,
                 no matter where you are in the country. From engines to headlights, we've got you covered.</p>
          </div>
        </div>
        <div class="col-lg-4 col-sm-6">
          <div class="item"> <span class="icon feature_box_col_three"><i class="fa fa-hourglass-half"></i></span>
            <h6>Nationwide Accessibility</h6>
            <p>If our customer has any problem,
            Our team of automotive experts is here to help. Whether you have questions about compatibility or installation, 
            rely on our knowledgeable staff to provide you with personalized support every step of the way.
            </p>
          </div>
        </div>
        
        
        
      </div>
    </div>
  </div>

        </div>
    </section>
</template>

<script setup>
useHead({
  link: [
    { 
      rel: 'stylesheet', 
      href: 'https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css',
      integrity: 'sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC',
      crossorigin: 'anonymous'
    }
  ]
})
const name = "jehan" ;
const {data: projects, pending1, error1} = useFetch('http://localhost:5000/Projects');
const {data: blogs, pending2, error2 } = useFetch('http://localhost:5000/Blogs');
</script>
<style>
/*added by jehan why choos us*/

h1,
h2,
h3,
h4,
h5,
h6 {}
a,
a:hover,
a:focus,
a:active {
    text-decoration: none;
    outline: none;
}

a,
a:active,
a:focus {
    color: #333;
    text-decoration: none;
    transition-timing-function: ease-in-out;
    -ms-transition-timing-function: ease-in-out;
    -moz-transition-timing-function: ease-in-out;
    -webkit-transition-timing-function: ease-in-out;
    -o-transition-timing-function: ease-in-out;
    transition-duration: .2s;
    -ms-transition-duration: .2s;
    -moz-transition-duration: .2s;
    -webkit-transition-duration: .2s;
    -o-transition-duration: .2s;
}

ul {
    margin: 0;
    padding: 0;
    list-style: none;
}
img {
max-width: 100%;
height: auto;
}
span, a, a:hover {
display: inline-block;
text-decoration: none;
color: inherit;
}
.section-head {
margin-bottom: 60px;
}
.section-head h4 {
position: relative;
padding:0;
color:#0261ae;
line-height: 1;
letter-spacing:0.3px;
font-size: 34px;
font-weight: 700;  
text-align:center;
text-transform:none;
margin-bottom:30px;
}
.section-head h4:before {
content: '';
width: 60px;
height: 3px;
background: #0261ae;
position: absolute;
left: 0px;
bottom: -10px;
right:0;  
margin:0 auto;
}
.section-head h4 span {
font-weight: 700;
padding-bottom: 5px;
color:#2f2f2f
}
p.service_text{
color:#cccccc !important;
font-size:16px;
line-height:28px;
text-align:center;    
}
.section-head p, p.awesome_line{
color:#818181;
font-size:16px;
line-height:28px;
text-align:center;  
}

.extra-text {
font-size:34px;
font-weight: 700;
color:#2f2f2f;
margin-bottom: 25px;
position:relative;
text-transform: none;
}
.extra-text::before {
content: '';
width: 60px;
height: 3px;
background: #0261ae;
position: absolute;
left: 0px;
bottom: -10px;
right: 0;
margin: 0 auto;
}
.extra-text span {
font-weight: 700;
color:#0261ae;
}
.item {
background: #fff;
text-align: center;
padding: 30px 25px;
-webkit-box-shadow:0 0px 25px rgba(0, 0, 0, 0.07);
box-shadow:0 0px 25px rgba(0, 0, 0, 0.07);
border-radius: 20px;
border:5px solid rgba(0, 0, 0, 0.07);
margin-bottom: 30px;
-webkit-transition: all .5s ease 0;
transition: all .5s ease 0;
transition: all 0.5s ease 0s;
}
.item:hover{
background:#0261ae;
box-shadow:0 8px 20px 0px rgba(0, 0, 0, 0.2);
-webkit-transition: all .5s ease 0;
transition: all .5s ease 0;
transition: all 0.5s ease 0s;
}
.item:hover .item, .item:hover span.icon{
background:#fff;
border-radius:10px;
-webkit-transition: all .5s ease 0;
transition: all .5s ease 0;
transition: all 0.5s ease 0s;
}
.item:hover h6, .item:hover p{
color:#fff;
-webkit-transition: all .5s ease 0;
transition: all .5s ease 0;
transition: all 0.5s ease 0s;
}
.item .icon {
font-size: 40px;
margin-bottom:25px;
color: #0261ae;   
width: 90px;
height: 90px;
line-height: 96px;
border-radius: 50px;
}
.item .feature_box_col_one{
background:rgba(247, 198, 5, 0.20);
color:#0261ae
}
.item .feature_box_col_two{
background:rgba(255, 77, 28, 0.15);
color:#0261ae
}
.item .feature_box_col_three{
background:rgba(0, 147, 38, 0.15);
color:#0261ae
}
.item .feature_box_col_four{
background:rgba(0, 108, 255, 0.15);
color:#0261ae
}
.item .feature_box_col_five{
background:rgba(146, 39, 255, 0.15);
color:#0261ae
}
.item .feature_box_col_six{
background:rgba(23, 39, 246, 0.15);
color:#0261ae
}
.item p{
font-size:15px;
line-height:26px;
}
.item h6 {
margin-bottom:20px;
color:#2f2f2f;
}
.mission p {
margin-bottom: 10px;
font-size: 15px;
line-height: 28px;
font-weight: 500;
}
.mission i {
display: inline-block;
width: 50px;
height: 50px;
line-height: 50px;
text-align: center;
background: #0261ae;
border-radius: 50%;
color: #fff;
font-size: 25px;
}
.mission .small-text {
margin-left: 10px;
font-size: 13px;
color: #666;
}
.skills {
padding-top:0px;
}
.skills .prog-item {
margin-bottom: 25px;
}
.skills .prog-item:last-child {
margin-bottom: 0;
}
.skills .prog-item p {
font-weight: 500;
font-size: 15px;
margin-bottom: 10px;
}
.skills .prog-item .skills-progress {
width: 100%;
height: 10px;
background: #e0e0e0;
border-radius:20px;
position: relative;
}
.skills .prog-item .skills-progress span {
position: absolute;
left: 0;
top: 0;
height: 100%;
background: #0261ae;
width: 10%;
border-radius: 10px;
-webkit-transition: all 1s;
transition: all 1s;
}
.skills .prog-item .skills-progress span:after {
content: attr(data-value);
position: absolute;
top: -5px;
right: 0;
font-size: 10px;
font-weight:600;    
color: #fff;
background:rgba(0, 0, 0, 0.9);
padding: 3px 7px;
border-radius: 30px;
}
</style>