<template>
  <Tabs
    bg-color="#000"
    txt-color="#fff"
    width="500px"
    height="300px"
  >
    <Tab
      v-for="(tab, index) in tabs"
      :key="index"
      :title="tab.title"
      :tab-key="tab.key"
      :is-active="tab.key === tabCurrent"
      @onChangeTab="changeTabHandler"
    >
      <p>{{ tab.content }}</p>
    </Tab>
  </Tabs>
</template>

<script setup>
import Tabs from './components/Tabs.vue';
import Tab from './components/Tab.vue';
import { ref } from '@vue/reactivity';

const tabs = [
  {
    key: 'home',
    title: 'Home',
    content: '[Home]: Consequat occaecat ullamco amet non eiusmod nostrud dolore irure incididunt est duis anim sunt officia. Fugiat velit proident aliquip nisi incididunt nostrud exercitation proident est nisi. Irure magna elit commodo anim ex veniam culpa eiusmod id nostrud sit cupidatat in veniam ad. Eiusmod consequat eu adipisicing minim anim aliquip cupidatat culpa excepteur quis. Occaecat sit eu exercitation irure Lorem incididunt nostrud.'
  },
  {
    key: 'profile',
    title: 'Profile',
    content: '[Profile]: Ad pariatur nostrud pariatur exercitation ipsum ipsum culpa mollit commodo mollit ex. Aute sunt incididunt amet commodo est sint nisi deserunt pariatur do. Aliquip ex eiusmod voluptate exercitation cillum id incididunt elit sunt. Qui minim sit magna Lorem id et dolore velit Lorem amet exercitation duis deserunt. Anim id labore elit adipisicing ut in id occaecat pariatur ut ullamco ea tempor duis.'
  },
];

const tabCurrent = ref('home');
const changeTabHandler = (tabKey) => {
  tabCurrent.value = tabKey;
}

</script>
