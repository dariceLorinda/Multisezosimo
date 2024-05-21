<template>
  <div class="main-container">
    <SectionComponent
        v-for="(section, index) in sections"
        :key="index"
        :highlighted-article="section.highlightedArticle"
        :center-images="section.highlightedArticle.image"
        :bottom-articles="section.bottomArticles"
        :right-articles="section.rightArticles"
    />
  </div>
</template>

<script>
import SectionComponent from './SectionComponent.vue';

export default {
  components: {
    SectionComponent
  },
  data() {
    return {
      sections: [
        {
          highlightedArticle: {
            title: 'Michael Cohen back on the stand to wrap up Trump trial testimony',
            preview: 'Michael Cohen back on the stand to wrap up Trump trial testimony',
            date: '2024-05-19T14:00:00',
            image: '../assets/media/firstPart/20240520-111120-resized.jpg',
            showImage: false
          },
          centerImages: [
            'path/to/center1.jpg'
          ],
          bottomArticles: [
            {
              title: 'Bottom Article 1',
              date: '2024-05-19T12:00:00',
              image: '../assets/media/firstPart/gettyimages-2153273786.jpg',
              showImage: true
            },
            {
              title: 'Bottom Article 2',
              date: '2024-05-19T11:00:00',
              image: '../assets/media/firstPart/ap24116453104478.jpg',
              showImage: true
            }
          ],
          rightArticles: [
            {
              title: 'Right Article 1',
              date: '2024-05-19T10:00:00',
              image: 'path/to/right1.jpg',
              showImage: false
            },
            {
              title: 'Right Article 2',
              date: '2024-05-19T09:00:00',
              showImage: false
            },
            {
              title: 'Right Article 3',
              date: '2024-05-19T08:00:00',
              image: 'path/to/right2.jpg',
              showImage: false
            }
          ]
        },
        // Add more sections as needed
      ]
    };
  }
};
</script>

<style>
.main-container {
  padding: 20px;
}
</style>
