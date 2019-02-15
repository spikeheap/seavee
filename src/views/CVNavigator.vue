<template>
  <div>
    <CV :cv_data=cv_data></CV>
  </div>
</template>

<script>
import CV from '../components/CV'

// TODO: do this better!
import ryan_cv from '../data/ryan_brooks.json'

export default {
  data: function(){
    return {
      cv_data: ryan_cv
    }
  },
  components: {
    CV
  }
}
</script>
