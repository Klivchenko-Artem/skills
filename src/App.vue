<template>
  <div class="app">
    <appMenu
      v-for="(group, index) in groups"
      :key="index"
      :title="group.title"
      :items="group.items"
    />
  </div>
</template>

<script>
import appMenu from './components/down/vue/appMenu.vue';

export default {
  components: {
    appMenu
  },
  data() {
    return {
      groups: [
        {
          title: 'Buff',
          items: [
            { title: 'Speed Bonus 30%', image: require('./components/down/img/speedapp.png'), description: 'Increases the hero TFR by 30%' },
            { title: 'Protection Bonus 60%', image: require('./components/down/img/defapp.png'), description: 'Increases the champion defense score by 60%' },
            {title: 'Attack Bonus 50%', image: require('./components/down/img/atkapp.png'), description: 'Increases the hero ATK by 50%' }
          ]
        },
        {
          title: 'Debuff',
          items: [
            { title: 'The speed penalty is 30%', image: require('./components/down/img/speeddown.png'), description: 'Reduces the speed of the champion by 30%.' },
            { title: 'The protection penalty is 60%', image: require('./components/down/img/defdown.png'), description: 'Reduces the champion defense by 60%.' },
            {title: 'The attack penalty is 50%', image: require('./components/down/img/atkdown.png'), description: 'Reduces the champion attack by 50%.' }
          ]
        }
      ]
    };
  }
};
</script>

<style>
.app {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}
</style>
