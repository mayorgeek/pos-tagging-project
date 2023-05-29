<script setup>
const words = [
  {word: 'ta', meaning: 'Head', type: 'Noun'},
  {word: 'nuku', meaning: 'Eye', type: 'Noun'},
  {word: 'adu', meaning: 'Teeth', type: 'Noun'},
  {word: 'dee', meaning: 'Tongue', type: 'Noun'},
  {word: 'wutu', meaning: 'Body', type: 'Noun'},
  {word: 'agbasa', meaning: 'Skin', type: 'Noun'},
  {word: 'kanjo', meaning: 'Blood', type: 'Noun'},
  {word: 'nududu', meaning: 'Food', type: 'Noun'},
  {word: 'koli', meaning: 'Knee', type: 'Noun'},
  {word: 'hun', meaning: 'Heart', type: 'Noun'},
  {word: 'negbe', meaning: 'Back', type: 'Noun'},
  {word: 'gbako', meaning: 'Jaw', type: 'Noun'},
  {word: 'tò', meaning: 'Ear', type: 'Noun'},
  {word: 'mii', meaning: 'Feaces', type: 'Noun'},
  {word: 'sii', meaning: 'Water', type: 'Noun'},
  {word: 'hevi', meaning: 'Fish', type: 'Noun'},
  {word: 'azimi', meaning: 'Oil', type: 'Noun'},
  {word: 'tevi', meaning: 'Yam', type: 'Noun'},
  {word: 'agbade', meaning: 'Maize', type: 'Noun'},
  {word: 'ayiku', meaning: 'Beans', type: 'Noun'},
  {word: 'ataki', meaning: 'Pepper', type: 'Noun'},
  {word: 'klekle siso', meaning: 'Plantain', type: 'Noun'},
  {word: 'klekle', meaning: 'Banana', type: 'Noun'},
  {word: 'gbo', meaning: 'Orange', type: 'Noun'},
  {word: 'azi', meaning: 'Groundnut', type: 'Noun'},
  {word: 'ati', meaning: 'Tree', type: 'Noun'},
  {word: 'aman', meaning: 'Leaf', type: 'Noun'},
  {word: 'nakimion', meaning: 'FireWood', type: 'Noun'},
  {word: 'afi', meaning: 'Smoke', type: 'Noun'},
  {word: 'sizin', meaning: 'Water Pot', type: 'Noun'},
  {word: 'asio', meaning: 'Axe', type: 'Noun'},
  {word: 'gan', meaning: 'Iron (Metal)', type: 'Noun'},
  {word: 'zan', meaning: 'Mat', type: 'Noun'},
  {word: 'yinvi', meaning: 'Needle', type: 'Noun'},
  {word: 'avo', meaning: 'Cloth', type: 'Noun'},
  {word: 'aza', meaning: 'Cap', type: 'Noun'},
  {word: 'hononhom', meaning: 'Room', type: 'Noun'},
  {word: 'ho', meaning: 'House', type: 'Noun'},
  {word: 'ali', meaning: 'Road', type: 'Noun'},
  {word: 'ahi', meaning: 'Market', type: 'Noun'},
  {word: 'gle', meaning: 'Farm', type: 'Noun'},
  {word: 'zukan', meaning: 'Bush', type: 'Noun'},
  {word: 'to', meaning: 'River', type: 'Noun'},
  {word: 'tojihu', meaning: 'Boat', type: 'Noun'},
  {word: 'afututun', meaning: 'Dust', type: 'Noun'},
  {word: 'ji', meaning: 'Rain', type: 'Noun'},
  {word: 'heovo', meaning: 'Sun', type: 'Noun'},
  {word: 'kanli', meaning: 'Animal', type: 'Noun'},
  {word: 'gbo', meaning: 'Goat', type: 'Noun'},
  {word: 'agbo', meaning: 'Sheep', type: 'Noun'},
  {word: 'yibu', meaning: 'Cow', type: 'Noun'},
  {word: 'cuku', meaning: 'Dog', type: 'Noun'},
  {word: 'ajaka', meaning: 'Rat', type: 'Noun'},
  {word: 'nuene', meaning: 'That', type: 'Article'},
  {word: 'nueye', meaning: 'This', type: 'Article'},
  {word: 'mali-mali me', meaning: 'Soon', type: 'Article'},
  {word: 'vii', meaning: 'Here', type: 'Article'},
  {word: 'blome', meaning: 'In', type: 'Preposition'},
  {word: 'nudida', meaning: 'Cooking', type: 'Verb'},
  {word: 'amlodido', meaning: 'Sleep', type: 'Verb'},
  {word: 'yazo', meaning: 'Work', type: 'Verb'},
  {word: 'jihan', meaning: 'Sing', type: 'Verb'},
  {word: 'dunu', meaning: 'Eat', type: 'Verb'},
  {word: 'nunu', meaning: 'Drink', type: 'Verb'},
  {word: 'minu', meaning: 'Swallow', type: 'Verb'},
  {word: 'didonu', meaning: 'Lick', type: 'Verb'},
  {word: 'donukpon', meaning: 'Taste', type: 'Verb'},
  {word: 'vinu', meaning: 'Vomit', type: 'Verb'},
  {word: 'dado', meaning: 'Urinate', type: 'Verb'},
  {word: 'jivi', meaning: 'Give Birth', type: 'Verb'},
  {word: 'eku', meaning: 'Die', type: 'Verb'},
  {word: 'chite', meaning: 'Stand', type: 'Verb'},
  {word: 'siagni', meaning: 'Sit', type: 'Verb'},
  {word: 'yii', meaning: 'Go', type: 'Verb'},
  {word: 'wa', meaning: 'Come', type: 'Verb'},
  {word: 'hiome', meaning: 'Enter', type: 'Verb'},
  {word: 'heji', meaning: 'Climb', type: 'Verb'},
  {word: 'kenwezu', meaning: 'Run', type: 'Verb'},
  {word: 'lon', meaning: 'Jump', type: 'Verb'},
  {word: 'zon', meaning: 'Fly', type: 'Verb'},
  {word: 'duwe', meaning: 'Dance', type: 'Verb'},
  {word: 'dayihu', meaning: 'Play', type: 'Verb'},
  {word: 'dogbe', meaning: 'Greet', type: 'Verb'},
  {word: 'hohu', meaning: 'Fight', type: 'Verb'},
  {word: 'yoio', meaning: 'Call', type: 'Verb'},
  {word: 'eclolo', meaning: 'Big', type: 'Adjective'},
  {word: 'kpevi', meaning: 'Small', type: 'Adjective'},
  {word: 'ga', meaning: 'Long', type: 'Adjective'},
  {word: 'gli', meaning: 'Short', type: 'Adjective'},
  {word: 'non wowo', meaning: 'Old', type: 'Adjective'},
  {word: 'non hoho', meaning: 'New', type: 'Adjective'},
  {word: 'non vifa', meaning: 'Wet', type: 'Adjective'},
  {word: 'non huhu', meaning: 'Dry', type: 'Adjective'},
  {word: 'non miodohu', meaning: 'Hot', type: 'Adjective'},
  {word: 'vifa', meaning: 'Cold', type: 'Adjective'},
  {word: 'non dagbe', meaning: 'Good', type: 'Adjective'},
  {word: 'non gblegble', meaning: 'Bad', type: 'Adjective'},
  {word: 'non vivi', meaning: 'Tasty', type: 'Adjective'},
  {word: 'non kpikpin', meaning: 'Heavy', type: 'Adjective'},
  {word: 'non gigo', meaning: 'Full', type: 'Adjective'},
];

const searchText = ref('');
const wordMeaning = ref('');
const wordPartOfSpeech = ref('');
const wordExist = ref(false);
const sentenceMeaning = ref([]);
const sentenceWordTypes = ref([]);

const search = () => {
  let data = words.filter(e => e.word.toLowerCase() === searchText.value.toLowerCase());
  if (data.length > 0) {
    sentenceMeaning.value = [];
    sentenceWordTypes.value = [];
    wordExist.value = true;
    wordMeaning.value = data[0].meaning;
    wordPartOfSpeech.value = data[0].type;
  } else {
    wordMeaning.value = '';
    wordPartOfSpeech.value = '';
    wordExist.value = false;
    sentenceMeaning.value = [];
    sentenceWordTypes.value = [];
    let sentenceWords = searchText.value.split(' ');
    for (let word of sentenceWords) {
      let temp = words.filter(e => e.word.toLowerCase() === word.toLowerCase());
      sentenceMeaning.value.push(temp[0].meaning);
      sentenceWordTypes.value.push(temp[0].type);
    }
  }
};

const clearData = () => {
  if (searchText.value === '') {
    sentenceMeaning.value = [];
    sentenceWordTypes.value = [];
    wordMeaning.value = '';
    wordPartOfSpeech.value = '';
    wordExist.value = false;
  }
};
</script>

<template>
  <div class="min-h-screen pt-32 bg-neutral-100">
    <h1 class="text-gray-800 font-bold text-2xl text-center mb-8 uppercase tracking-wide">Part Of Speech Tagging</h1>
    <div class="max-w-2xl mx-auto border border-gray-300 rounded px-6 py-12 lg:p-12 bg-white">
      <!-- Search Area -->
      <div class="flex items-center space-x-2">
        <input
            v-model="searchText"
            id="search_text"
            type="text"
            list="suggestions"
            placeholder="Start Typing A Word..."
            class="block text-gray-800 w-full h-16 px-4 border border-gray-300"
            @change="clearData"
        >
        <button
            @click="search"
            type="button"
            class="h-16 w-16 text-center cursor-default inline-flex items-center px-4 py-2 bg-indigo-600 active:bg-indigo-700 focus:bg-indigo-700 border border-transparent rounded-md font-semibold text-xs text-white uppercase tracking-widest hover:bg-indigo-700 focus:bg-gray-700 active:bg-indigo-900 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 transition ease-in-out duration-150"
        >
          Go
        </button>
      </div>

      <div class="mt-8" v-if="wordPartOfSpeech">
        <p>The word "<span class="font-bold">{{searchText}}</span>" is a {{wordPartOfSpeech}}</p>
      </div>

      <div v-if="wordMeaning" class="mt-8 flex items-center space-x-8 text-lg">
        <h2 class="text-gray-800 font-medium">Word Meaning: </h2>
        <p class="text-blue-500 font-semibold">{{wordMeaning}}</p>
      </div>

      <div v-if="sentenceWordTypes.length > 0" class="mt-8 flex items-center space-x-8 text-lg">
        <h2 class="text-gray-800 font-medium">Word Composition: </h2>
        <div class="space-x-2">
          <span class="text-blue-500 font-semibold" v-for="(wordType, index) in sentenceWordTypes">{{wordType}} <span v-if="index != sentenceWordTypes.length - 1">+</span></span>
        </div>
      </div>

      <div v-if="sentenceMeaning.length > 0" class="mt-8 flex items-center space-x-8 text-lg">
        <h2 class="text-gray-800 font-medium">Sentence Meaning: </h2>
        <div class="space-x-2">
          <span class="text-blue-500 font-semibold" v-for="meaning in sentenceMeaning">{{meaning}}</span>
        </div>
      </div>
    </div>
  </div>
</template>
