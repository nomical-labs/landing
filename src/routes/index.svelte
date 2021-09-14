<script>
	import { onMount } from 'svelte';
  import '../styles/global.css'
  import Footer from '../components/footer.svelte';
  import ProjectItem from '../components/projectItem.svelte';
  let contactForm
  onMount(()=>{
    console.log(contactForm)
  contactForm.addEventListener("submit", handleSubmit);
  })
  const handleSubmit = (e) => {
    e.preventDefault()
    let myForm = contactForm
    let formData = new FormData(myForm)
    fetch('/', {
      method: 'POST',
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams(formData).toString()
    }).then(() => console.log('Form successfully submitted')).catch((error) =>
      alert(error))
  }

</script>
<style>
h1,h2 {
  font-family: 'Mulish', sans-serif;
}
h1 {
  font-weight: 900;
  margin-top: 0;
  font-size: 45px;
  line-height: 1.25;
}

.hero {
  padding: 1rem;
}
.hero--inner {
  text-align: left;
  padding: 4rem 20%;
}
.headlogo {
  max-width: 6rem;
  margin: 1rem 0;
}
/* Util Classes */
.flex {
  display: flex;
}
.flex-center {
  justify-content: center;
}
.text-center {
  text-align: center;
}
.contact-form {
  display: flex;
  align-items: stretch;
  justify-content: center;
}
.contact-form > input {
  min-width: 0;
  font-size: 16px;
  border: 1px solid rgb(216, 216, 216);
  padding-left: 15px;
  padding-right: 15px;
  padding-top: 13px;
  padding-bottom: 13px;
  border-radius: 10px;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.contact-form > button {
  min-width: 0;
  font-size: 16px;
  border: 1px solid rgb(216, 216, 216);
  color: white;
  font-weight: 700;
  padding-bottom: 15px;
  padding-left: 25px;
  padding-right: 25px;
  padding-top: 15px;
  background-color: rgb(35,39,42);
  border-radius: 10px;

  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}

h4 {
  margin-top: 40px;
  margin-bottom: 10px;
}
h2 {
  color: rgb(109, 109, 109);
}
/*
.projects {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
@media only screen and (min-width: 700px) {
  .projects {
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 12px;
  }
}
.wrapper {
  max-width: 1024px;
  margin: auto;
  padding: 0 1rem;
}
*/
</style>
<svelte:head>
	<link href="/assets/logo.svg" rel="icon">
  <title>nomical labs</title>
</svelte:head>

<section class="hover-inner">
  <div class="hero">
    <div class="flex flex-center">
      <object title="Logo" data="../assets/logo.svg" class="headlogo"></object>
    </div>
    <div class="hero--inner text-center">
      <h1>more software ariving in 3-5 business days.</h1>
      <h2>currently writing lines of code.</h2>
      <h4>contact us and we'll get back to you</h4>
      <form class="contact-form" bind:this={contactForm} name="Contact Form">
        <input name="email" type="email" placeholder="email address">
        <button type="submit">contact us</button>
      </form>
      
    </div>
    <!--<div class="wrapper">
      <div class="projects-outer">
        <div class="projects">
          <ProjectItem logo="/assets/SwagChat/logo.png" link="https://swag-chatv5.vercel.app/?ref=nomical" title="SwagChatv5" description="SwagChatv5 is a decentralised chat messaging platform for highly restricted networks."/>
          <ProjectItem disabled logo="/assets/SwagChat/logo.png" link="https://swag-chatv5.vercel.app/?ref=nomical" title="SwagChatv5" description="SwagChatv5 is a decentralised chat messaging platform for highly restricted networks."/>
        </div>
      </div>
    </div>
    
    Coming soon...
    Reading this? Contribute. https://github.com/nomical-labs
    -->

  </div>
</section>
<span style="height: 5rem; width: 5rem; display: block"></span>
<Footer />