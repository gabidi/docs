<template lang="pug">
  component-view(v-bind:doc="doc")
</template>

<script>
  export default {
    data () {
      return {
        doc: {
          title: 'Forms',
          component: 'forms',
          edit: 'FormView',
          desc: 'Forms and stuff',
          examples: [
            { header: "VForm - Basic validation", file: "forms/1", desc: '' },
            { header: "VForm - Validation w/ submit & clear", file: "forms/2", desc: '' },
            { header: "Vuelidate", file: "forms/3", desc: '' },
            { header: "Vee-validate", file: "forms/4", desc: '' }
          ],
          props: {
            'v-form': {
              params: [
                [
                  'value',
                  'Boolean',
                  'false',
                  'Current validation state of form'
                ]
              ],
              model: {
                type: 'Boolean',
                default: 'false',
                description: 'Current validation state of form'
              }
            }
          },
          slots: {
            'v-form': {
              shared: ['default']
            }
          },
          events: {
            'v-form': {
              params: [
                ['input', 'Boolean', 'Validation state changed']
              ]
            },
          }
        }
      }
    },
  }
</script>

<style lang="stylus">
</style>
