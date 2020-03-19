<template>

<div class="menu-item" @click="isOpen = !isOpen" tabindex="22" offset="25" >
 


    <a href="#"> 
        {{title}}
    </a>
    <svg viewBox="0 0 1030 638" width="10">
        <path d="M1017 68L541 626q-11 12-26 12t-26-12L13 68Q-3
        49 6 24.5T39 0h952q24 0 33 24.5t-7 43.5z"
        fill="#ca361c"></path>
    </svg>
    <transition name='fade' appear>
        <div class="sub-menu" v-if="isOpen">
            <div v-for="(item, i) in items" :key='i' class="menu-item">
                <a href="item.link">{{item.title}}</a>
            </div>
         </div>
    </transition>
    </div>
</template>



<script> 
export default {
    name: 'dropdown',
    props: ['title', 'items'],
    data() {
        return {
            isOpen: false
        }
    }
}

</script>


<style scope>
nav .menu-item svg{
    width: 13px;
    margin-left: 5px;
}
nav .menu-item .sub-menu {
    
    position: absolute;
    will-change: transform;
    min-width: 9em;
    background-color: rgb(229, 226, 226);
    top: calc(100% + 15px);
    left: 50%;
    transform:  translateX(-50%);
    width: max-content;
    border-radius: 0px 0px 16px 16px;
}
   
    
    





.fade-enter-active,
.fade-leave-active{
    transition: all .1s ease-out;
}

.fade-enter,
.fade-leave-to{
    opacity: 0;
}
    
</style>