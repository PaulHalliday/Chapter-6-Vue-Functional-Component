<script>
import ListItem from './components/ListItem.vue';

export default {
  data() {
    return {
      names: ['Evan You', 'Edd Yerburgh', 'Paul Halliday']
    }
  },
  render(createElement) {
    return createElement('div', [
           createElement('ul',
            this.names.map(name => 
              createElement(ListItem, 
                {props: { name: name }
              })
          ))])
  }
}
</script>