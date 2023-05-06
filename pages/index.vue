<template lang="pug">
div
  q-splitter(
    v-model="splitterModel"
    style="height: 100vh"
  )

    template(
      v-slot:before
    )
      div.q-pa-md
        div.text-h4.q-mb-md Before
        div(
          v-for="n in 20" 
          :key="n" 
          class="q-my-md"
        ) {{ n }}. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.

    template(
      v-slot:after
    )
      q-splitter(
        v-model="insideModel"
        horizontal
      )

        template(
          v-slot:before
        )
          div.q-pa-md
            div.text-h4.q-mb-md Before
            div(
              v-for="n in 20" 
              :key="n" 
              class="q-my-md") {{ n }}. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.

        template(
          v-slot:after
        )
          div.q-pa-md
            div.text-h4.q-mb-md After
            div(
              v-for="n in 20" 
              :key="n" 
              class="q-my-md"
            ) {{ n }}. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      splitterModel: ref(50), // start at 50%
      insideModel: ref(50)
    }
  }
}
</script>
