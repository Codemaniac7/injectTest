<template>
    <ul>
        <!-- <li v-for="s in songs"></li> -->
        
        <SongListItem v-for="s in songs" :key="s.id" :song="s"/>
        <div>체크된 곡 수 : {{ doneCount }}</div>
    </ul>

</template>

<script>
import SongListItem from './SongListItem.vue';
export default {
    name:'SongList',
    components: {SongListItem},
    props: ['songs'],
    inject: ['doneCount']
}
</script>