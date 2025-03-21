<template>
<NavigationBar/>
<HeaderMainContent/>
<HeaderCategoryContent/>
</template>

<script>

import NavigationBar from "./navigation-bar/navigation-bar.vue"
import HeaderCategoryContent from "./header-category-content/header-category-content.vue"
import HeaderMainContent from "./header-main-content/header-main-content.vue"

export default {
  name: 'headerSection',
  props: {
    msg: String
  },
    components: {
    NavigationBar,
    HeaderCategoryContent,
    HeaderMainContent
  }
}
</script>
