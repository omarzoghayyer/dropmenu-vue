<template>
    <nav>
        
    <div class="menu-item"><a href="">Home</a></div>
    <div class="menu-item"><a href="">Contact</a></div>
    <Dropdownmenu title="Services" :items="services"/>
    <div class="menu-item"><a href="">About</a></div>

    </nav>
</template>


<script>
import Dropdownmenu from './Dropdownmenu'
export default {
    name: 'Navbar',
    components: {
        Dropdownmenu
    },
    data() {
        return {
            services:[
                {
                    title: 'Web',
                    link: '#'
                },
                {
                    title: ' Design',
                    link: '#'
                },
                {
                    title: 'Videos',
                    link: '#'
                },
                {
                    title: 'Videos',
                    link: '#'
                },
                {
                    title: 'Videos',
                    link: '#'
                },
                {
                    title: 'Videos',
                    link: '#'
                }
            ]
        }
    }
}
</script>

<style scope>
nav{
    display: flex;
    align-items:center;
    justify-content: center;
}
nav .menu-item{
    color: rgb(221, 215, 215);
    padding: 10px 20px;
    position: relative;
    text-align: center;
    border-bottom: 3px solid transparent;
    display: block;
    transition: 0.5s; 
}
nav .menu-item a{
    color:rgb(136, 13, 13);
    text-decoration: none;
}
nav .menu-item :active,
nav .menu-item:hover {
    background-color: rgb(236, 231, 231);
    border-bottom-color: red;
}

    
</style>