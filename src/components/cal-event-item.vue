<template>
<div class="wrapper" :class="{lab : event.customClass === 'lab', other : event.customClass === 'other', conversation : event.customClass === 'conversation'}">
  <div class="time">
    <!-- <p>{{dateTimeFormatter(Date.parse(new Date(event.date)),i18n[locale].fullFormat)}}</p> -->
    <p>{{event.time}}</p>
  </div>
  <div class="title">
    {{event.title}}
  </div>

</div>
</template>



<script>
import i18n from '../i18n.js'
import { dateTimeFormatter } from '../tools.js'
export default {
  data() {
    return {
      i18n
    }
  },
  props: {
    event: {
      type: Object,
      required: true
    },
    index: {
      type: Number,
      required: true
    },
    locale: {
      type: String,
      required: true
    }
  },
  methods: {
    dateTimeFormatter
  }
}
</script>
