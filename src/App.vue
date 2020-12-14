<template>
  <v-container>
    <tiptap-vuetify
      v-model="content"
      :extensions="extensions" />

  </v-container>
</template>

<script>

// import the component and the necessary extensions
import { TiptapVuetify, Heading, Bold, Italic, Strike, Underline, Code, Paragraph, BulletList, OrderedList, ListItem, Link, Blockquote, HardBreak, HorizontalRule, History ,TodoList,TodoItem} from 'tiptap-vuetify'

export default {
  // specify TiptapVuetify component in "components"
  components: { TiptapVuetify },

  data: () => ({
    content: `
      <h3>TIPTAP</h3>`,
    // declare extensions you want to use
    extensions: [
      History,
      Blockquote,
      Link,
      Underline,
      Strike,
      Italic,
      ListItem,
      BulletList,
      OrderedList,
      [Heading, {
        options: {
          levels: [1, 2, 3]
        }
      }],
      Bold,
      Code,
      HorizontalRule,
      Paragraph,
      HardBreak,
      TodoList,
      [TodoItem, {
        options: {nested: true}
      }],],  
  }),}
</script>