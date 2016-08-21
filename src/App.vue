<template>
  <accordion-example></accordion-example>
</template>

<script>
import accordionExample from './example'
import { accordion, accordionItem } from '../release/vue-accordion'

console.log(accordion)
console.log(accordionItem)

export default {
  components: {
    accordionExample
    // VueProgressBar
  }
}
</script>
