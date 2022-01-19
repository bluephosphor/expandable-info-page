<script>
	import InfoBox from './InfoBox.svelte';
</script>

<main id="container">
	<InfoBox 
    img="clouds.jpg" 
    title="Noticulcent clouds"
    info="Noticulcent clouds are a rare illusion phenomenon. They appear on the shy whenever astronomical light is present and it reflects from ground ice in the clouds."
  />
  <InfoBox 
    img="supermassive.jpg"
    title="Black Hole (Messier 87)"
    info="The supermassive black hole at the core of supergiant elliptical galaxy Messier 87, with a mass about 7 billion times that of the Sun, as depicted in the first false-colour image in radio waves released by the Event Horizon Telescope (10 April 2019)."
  />
  <InfoBox 
    img="etacar.jpg"
    title="Eta Carinae"
    info="Eta Carinae, a volatile system containing two massive stars that closely orbit each other. This image has three types of light: optical data from Hubble (appearing as white), ultraviolet (cyan) from Hubble, and X-rays from Chandra (appearing as purple emission). The previous eruptions of this star have resulted in a ring of hot, X-ray emitting gas about 2.3 light years in diameter surrounding these two stars."
  />
  <InfoBox 
    img="gal4.jpg"
    title="NGC 2336"
    info="NGC 2336 is the quintessential galaxy — big, beautiful, and blue — and it is captured here by the NASA/ESA Hubble Space Telescope. The barred spiral galaxy stretches an immense 200,000 light-years across and is located approximately 100 million light-years away in the northern constellation of Camelopardalis (the Giraffe)."
  />
</main>

<style>
  #container{
    background: white;
    display: flex;
    flex-wrap: wrap;
    width: 90vw;
    max-width: 950px;
    align-items: space-between;
    justify-content: space-between;
    row-gap: 16px;
    margin: 32px auto;
    padding:12px;
  }
  @media screen and (max-width: 900px) {
    #container{
      margin: none;
      align-items: stretch;
      flex-flow: column nowrap;
    }
  }
</style>