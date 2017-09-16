<meta content='width=device-width, initial-scale=1' name='viewport'>
<link href='https://fonts.googleapis.com/css?family=Roboto:100,200,300,400italic,400,500,500italic,700,700italic,900%7CMaterial+Icons' rel='stylesheet' type='text/css'/>
<style>
body {
  background-color:white;
  margin:0;
  padding:0 30px;
  color:#212121;
  font-family:'Roboto',sans-serif;
}
.contact-box{
  overflow:hidden;
}
h1,h2,h3{
  text-align:center;
}
#contactForm input:focus~label,#contactForm input:valid~label,#contactForm textarea:focus~label,#contactForm textarea:valid~label{font-size:.75em;color:red;top:-2.25rem;-webkit-transition:all 125ms ease;transition:all 125ms ease}
#contactForm .styled-input{float:left;width:33.3333%;margin:2rem 0 0;padding:0 10px 0 0;position:relative;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;box-sizing:border-box}
#contactForm .styled-input-in{position:relative}
#contactForm{margin-right:-10px}
#contactForm .styled-input label{color:#999;padding:1rem;position:absolute;top:0;left:0;-webkit-transition:all .25s ease;transition:all .25s ease;pointer-events:none;line-height:1}
#contactForm .styled-input.wide{width:100%}
#contactForm input,#contactForm textarea{font-family:'Roboto',sans-serif;padding:1rem;border:1px solid #ddd;width:100%;font-size:1rem;background:#fafafa;-moz-box-sizing:border-box;-webkit-box-sizing:border-box;box-sizing:border-box}
#contactForm input~.span1,#contactForm textarea~.span1{display:block;width:0;height:3px;background:red;position:absolute;left:50%;-webkit-transition:width .4s ease-in-out;transition:width .4s ease-in-out}
#contactForm input~.span2,#contactForm textarea~.span2{display:block;width:0;height:3px;background:red;position:absolute;right:50%;-webkit-transition:width .4s ease-in-out;transition:width .4s ease-in-out}
#contactForm input~span{bottom:0}
#contactForm textarea~span{bottom:0}
#contactForm input:focus,#contactForm textarea:focus{outline:0}
#contactForm input:focus~.span1,#contactForm input:focus~.span2,#contactForm textarea:focus~.span1,#contactForm textarea:focus~.span2{width:50%}
#contactForm textarea{width:100%;min-height:15em}
#contactForm .btn{font-family:Helvetica,Arial,sans-serif;text-transform:uppercase;font-size:14px;font-weight:800;letter-spacing:1px;border-radius:0;padding:0 25px;height:51px;line-height:51px;color:#333;background-color:#fafafa;border:1px solid #ddd;cursor:pointer;margin:20px 0 0;background-image:none}
#contactForm .btn-default:focus,#contactForm .btn-default:hover{background-color:red;border:1px solid #c40303;color:#fff}
#contactForm .gotcha{border:none;background:0 0;display:none}
@media screen and (max-width:800px){#contactForm .styled-input {width:100%;}
}
</style>

<script>
function getQueryVariable(variable) {
  var query = window.location.search.substring(1);
  var vars = query.split("&");
  for (var i=0;i<vars.length;i++) {
    var pair = vars[i].split("=");
    if(pair[0] == variable){return pair[1];}
  }
  return(false);
}
var emailform = getQueryVariable("email");
var urlthanks = getQueryVariable("url");
var urlblog = getQueryVariable("blog");
var titleblog = getQueryVariable('title').replace(/%20/g, " ");
</script>
<div class="contact-box">
<h1>Contact Form</h1>
<script>
document.write('<h2>'+titleblog+'</h2>\
<form action="https://formspree.io/'+ emailform +'" method="POST" target="_blank" name="sentMessage" id="contactForm">\
<input type="hidden" name="_next" value="'+ urlthanks +'" />\
    <div class="styled-input">\
      <div class="styled-input-in">\
      <input type="text" name="name" required />\
      <label>Name</label>\
      <span class="span1"></span><span class="span2"></span> </div></div>\
    <div class="styled-input">\
      <div class="styled-input-in">\
      <input type="email" name="_replyto" required />\
      <label>Email</label>\
      <span class="span1"></span><span class="span2"></span> </div></div>\
    <div class="styled-input">\
      <div class="styled-input-in">\
      <input type="text" name="_subject" required />\
      <label>Subject</label>\
      <span class="span1"></span><span class="span2"></span> </div></div>\
    <div class="styled-input wide">\
      <div class="styled-input-in">\
      <textarea name="message" required></textarea>\
      <label>Message</label>\
      <span class="span1"></span><span class="span2"></span> </div></div>\
    <button type="submit" class="btn btn-default">Send</button>\
    <input type="text" name="_gotcha" class="gotcha" />\
  </form>\
  <h3>Back to <a href="'+ urlblog +'" title="Homepage">Homepage</a></h3>');
  </script>
</div>
