<template>
  <div>
    <h1>{{ title }}</h1>
    <h3>{{ taglines[Math.floor(Math.random() * taglines.length)].message }}</h3>
    <ul>
      <li v-for="link in links" v-bind:key="link.text">
        <a v-bind:href="link.url"
          target="_blank"
        >
          {{ link.text }}
        </a>
      </li>
      <br>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Welcome',
  data () {
    return {
      title: 'Kimball Bros',
      taglines: [
        { message: 'We \'dem boys' },
        { message: 'We do business' }
      ],
      links: [
        {
          text: 'Email',
          url: 'mailto:kimballbros@gmail.com'
        },
        {
          text: 'Github',
          url: 'https://github.com/KimballBros'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h3 {
    font-weight: normal;
  }
  ul {
    font-size: 14px;
    list-style-type: none;
    padding: 0px;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #123191;
  }
</style>
