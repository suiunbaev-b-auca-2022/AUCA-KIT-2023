<!-- src/routes/About.svelte -->
<script>
  export let services = [
    {
      title: "Web Design",
      description:
        "Web design refers to the design of websites that are displayed on the internet. It usually refers to the user experience aspects of website development rather than software development. Web design used to be focused on designing websites for desktop browsers; however, since the mid-2010s, design for mobile and tablet browsers has become ever-increasingly important.",
      imageSrc:
        "https://miro.medium.com/v2/resize:fit:828/format:webp/1*aTYOTFS4Vkr-nwHNML3GvQ.jpeg",
    },
    {
      title: "Graphic Design",
      description:
        "Graphic design is a craft where professionals create visual content to communicate messages. By applying visual hierarchy and page layout techniques, designers use typography and pictures to meet users’ specific needs and focus on the logic of displaying elements in interactive designs, to optimize the user experience.",
      imageSrc:
        "https://www.postalplussuwanee.com/portals/98/StoreFiles/design2.jpg",
    },
    {
      title: "Search Engine Optimization",
      description:
        "Search engine optimization (SEO) is the art and science of getting pages to rank higher in search engines such as Google. Because search is one of the main ways in which people discover content online, ranking higher in search engines can lead to an increase in traffic to a website.",
      imageSrc:
        "https://www.lemonlight.com/wp-content/uploads/2023/01/AdobeStock_275879381-768x485.jpeg",
    },
  ];
</script>

<section class="about-page">
  <h2>About Us</h2>

  {#each services as { title, description, imageSrc }}
    <div class="service">
      <img src={imageSrc} alt={title} />
      <div>
        <h3>{title}</h3>
        <p>{description}</p>
      </div>
    </div>
  {/each}
</section>

<style>
  /* Add your existing styles here */
  .about-page {
    margin: 20px;
  }

  .service {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    gap: 20px;
    border: 1px solid #ddd;
    margin-bottom: 20px;
  }

  .service img {
    width: 300px;
    height: auto;
  }

  .service h3 {
    font-size: 24px;
    margin-bottom: 10px;
  }

  .service p {
    font-size: 16px;
  }
</style>
