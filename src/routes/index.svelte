<script>
  import '../styles/global.css'
  import Footer from '../components/footer.svelte';
  import ProjectItem from '../components/projectItem.svelte';
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
<Footer />