<template>
    <div>
        <Header text="Ini Adalah Header">
            <template #footer>
                <p>Ini Adalah Slot Dari Footer</p>
            </template>
        </Header>
        <MyComponent nama="sarah" umur="16"></MyComponent>
        <LatihanComponent name="sarah" age="19"></LatihanComponent>
        <LatihanDuaComponent></LatihanDuaComponent>
        <WatchersComponent nama="sarahh" umur="24"></WatchersComponent>
        <h2>Event Component</h2>
        <latihan-event-component :nama="nama" :umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            <template #header>
                <div>
                    <p>Ini Adalah Header latihan Event</p>
                </div>
            </template>
        </latihan-event-component>
    </div>
</template>

<script setup>
import LatihanEventComponent from './icons/LatihanEventComponent.vue';
import MyComponent from './MyComponent.vue'
import LatihanComponent from './LatihanComponent.vue';
import LatihanDuaComponent from './icons/LatihanDuaComponent.vue';
import WatchersComponent from './icons/WatchersComponent.vue';

//event
import { ref } from 'vue';
const nama = ref('Fitri');
const umur = ref(25);

const onGreeted = () => {
    console.log('Kamu udah disapa, bro!');
};

// export default {
//     compo nents :{
//        header
//     }
// }
</script>

<style>
h1{
    color: blue;
}
p{
    size: 16px;
}
</style>