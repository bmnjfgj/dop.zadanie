<template>
  <div class="container">
    <h1 class="header">Character Information</h1>
    <character-header :image-src="imageSrc" :personal-data="personalData"></character-header>
    <biography-section :biography-paragraphs="biography" :phrases="catchphrases"></biography-section>
  </div>
</template>

<script>
import CharacterHeader from './CharacterHeader.vue';
import BiographySection from './BiographySection.vue';
import image from './images.png';

export default {
  name: 'App',
  components: {
    CharacterHeader,
    BiographySection
  },
  data: function () {
    return {
      imageSrc: image,
      personalData: [
        {type: 'Name', value: 'SpongeBob SquarePants'},
        {type: 'Age', value: 26},
        {type: 'Sex', value: 'Male'},
        {type: 'Skin color', value: 'Yellow', color: 'yellow'},
        {type: 'Eyes color', value: 'Blue', color: 'blue'},
        {type: 'Driver License Class', value: 'S'}
      ],
      biography: [
        'SpongeBob SquarePants (born July 14, 1986[13]) is the titular main protagonist of the animated series of the same name. He was designed by show creator and former marine biologist, the late Stephen Hillenburg. Stephen Hillenburg based SpongeBob on Bob the Sponge, a character he had created for his educational book The Intertidal Zone in 1984.',
        'SpongeBob is a childish, joyful, hardworking, and sometimes clumsy and silly sea sponge who lives in a pineapple with his pet snail Gary in the underwater city of Bikini Bottom. He works as a fry cook at the Krusty Krab, a job in which he is exceptionally skilled at and enjoys thoroughly. He attends Mrs. Puff\'s Boating School, and his greatest dream in life is to receive his boating license. Unfortunately, he tenses up whenever he has to drive a boatmobile, and he drives recklessly by speeding, crashing into buildings, etc., which causes him to fail every time. SpongeBob is very good-natured and loves to hang out with his best friend, Patrick. His teacher is Mrs. Puff and his boss is Mr. Krabs.',
        'Like real sea sponges, SpongeBob has the ability to filter-feed (as shown in "I Had an Accident") and reproduce by budding (in "Naughty Nautical Neighbors"). In The SpongeBob Musical, SpongeBob\'s exact species of sea sponge is identified: Aplysina fistularis, a yellow sea sponge that is commonly found in open waters. [14]',
        'SpongeBob appears in most episodes of the series, beginning with the series\' debut episode, "Help Wanted." He is voiced by Tom Kenny, who is married to Karen Plankton\'s voice actress, Jill Talley.'
      ],
      catchphrases: [
        'I\'m ready!',
        'Order up',
        'Aye-aye, captain!',
        'Barnacles!',
        'Tartar sauce',
        'Fish paste',
        'Hoppin clams!',
        'Jumping jellyfish!',
        'Hi Squidward.',
        'Hey Squidward',
        'May I take your order?'
      ]
    };
  }
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  background-color: #fffacd;
  color: #000;
  margin: 0;
  padding: 0;
}
.container {
  max-width: 800px;
  margin: 0 auto;
  min-height: 100vh;
  background-color: #fffacd;
  padding: 20px;
  box-sizing: border-box;
}
.header {
  text-align: center;
  border-bottom: 1px solid #ccc;
  padding-bottom: 10px;
  margin-bottom: 20px;
}
</style>