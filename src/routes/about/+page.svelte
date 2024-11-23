


<svelte:head>
	<title>Samuel Strickland — About</title>
</svelte:head>


<h1>About Me</h1>
<p>This should really tell you everything about me.</p>


<div class="container">
    <iframe class="responsive-iframe" src="https://docs.google.com/document/d/e/2PACX-1vSEz8EdfWOaC8ZJJIs-Bxe1MJQaZta5ADPHGUaa57XSn1hinf6KpEj0HGo0eqP0PRpFPzDSRv_qyBw-/pub?embedded=true" title="PDF"> </iframe>
</div>


<style>
    .container {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding-top: 56.25%; /* 16:9 Aspect Ratio (divide 9 by 16 = 0.5625) */
}
    .responsive-iframe {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
}

</style>