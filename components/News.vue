<template>
  <div class="latest-news">
    <div class="featured-news">
      <div class="featured-news-item">
        <h2>{{ featuredNews.title }}</h2>
        <p>{{ featuredNews.description }}</p>
        <small>{{ formatDate(featuredNews.date) }}</small>
      </div>
    </div>
    <div class="other-news">
      <ul>
        <li v-for="news in otherNews" :key="news.id">
          <h3>{{ news.title }}</h3>
          <p>{{ news.description }}</p>
          <small>{{ formatDate(news.date) }}</small>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      featuredNews: {
        id: 1,
        title: 'Notícia Destacada',
        description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam in congue lorem, at consectetur erat. Proin tempus, ex vitae viverra tincidunt, ipsum felis ultricies quam, quis fermentum nisl massa ac tortor. Nullam ac aliquam nunc. Vivamus congue porta dolor at molestie. Donec sodales mauris nisi, ac tincidunt ex porttitor ut. Sed non urna ut leo bibendum dignissim. Duis sed pulvinar dolor. Donec et leo sed tellus posuere sagittis. Suspendisse quis magna id augue ornare mollis. Sed lobortis turpis lorem, sed venenatis urna porta nec. Integer tempus est neque, et posuere arcu tincidunt non. Mauris congue urna et justo ornare, in pretium urna finibus. Fusce eget tincidunt tellus. Fusce posuere dictum nisl, quis scelerisque purus suscipit ac. Mauris sagittis, nunc a bibendum imperdiet, turpis tortor lacinia lorem, convallis rutrum nisl nibh lacinia est. Sed vel lorem tempus, imperdiet diam vel, rutrum orci. Sed a faucibus massa. Aenean eget erat justo. Maecenas nisi lorem, malesuada dapibus rhoncus a, accumsan et felis. Quisque eleifend tincidunt leo at sollicitudin. Maecenas ornare justo a porttitor euismod. Proin aliquet tortor orci, non egestas urna molestie in.",
        date: '2023-12-05',
      },
      otherNews: [
        {
          id: 2,
          title: 'Notícia 1',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse ac augue in neque tincidunt consectetur. Pellentesque pretium sollicitudin orci ut..',
          date: '2023-12-01',
        },
        {
          id: 3,
          title: 'Notícia 2',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse ac augue in neque tincidunt consectetur. Pellentesque pretium sollicitudin orci ut..',
          date: '2023-11-28',
        },
        {
          id: 4,
          title: 'Notícia 3',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse ac augue in neque tincidunt consectetur. Pellentesque pretium sollicitudin orci ut..',
          date: '2023-11-25',
        },
      ],
    };
  },
  methods: {
    formatDate(date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' };
      return new Date(date).toLocaleDateString('pt-BR', options);
    },
  },
};
</script>

<style scoped>
.latest-news {
  display: flex;
  max-width: 100%;
  margin: 60px auto;
  box-sizing: border-box;
  text-align: left;
}

.featured-news {
  flex: 1;
  padding-right: 20px;
}

.featured-news-item {
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: 20px;
}

.other-news {
  flex: 1;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  border: 1px solid #ccc;
  border-radius: 10px;
  margin-bottom: 20px;
  padding: 20px;
}

h2 {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

h3 {
  font-size: 1.2rem;
  margin-bottom: 5px;
}

p {
  margin-bottom: 10px;
}

small {
  color: #777;
}
</style>
