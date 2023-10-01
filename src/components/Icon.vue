<!-- component that removes watermark and changes fill colour, while preserving the original icon-->
<template>
    <div>
      <div class="icon" v-html="svgContent"></div>
    </div>
  </template>
  
  <script>
  export default {
    name:"IconComponent",
    data() {
      return {
        svgContent: '' // SVG content will be stored here
      };
    },
    mounted() {
    // Fetch the SVG content when the component is mounted
    fetch(`/public/icons/${this.card.img}`)
      .then((response) => response.text())
      .then((svgData) => {
        // Remove text elements from the SVG content
        svgData = svgData.replace(/<text[^>]*>[\s\S]*?<\/text>/g, '');
        // Change the fill color of all paths to blue
        svgData = svgData.replace(/<path/g, `<path fill="${this.colour}" stroke="${this.colour}"stroke-width="0.5px"`);
        //svgData = svgData.replace(/<path/g, `<path fill="${this.colour}"`);
        //svgData = svgData.replace(/<path\s|<rect\s/g, `<path fill="${this.colour}"`).replace(/fill="#[0-9A-Fa-f]{6}"/g, '');
        this.svgContent = svgData;
      });
  },
    props: {
      card: {
        type: Object,
        required: true
      }, colour:String
    }
  };
  </script>
  