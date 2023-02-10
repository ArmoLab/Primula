<template>
    <header>
        <span class="title">Website (Preview)</span>
        <nav class="menu">
            <a 
                v-for="item in navigation" 
                :key="item.name" 
                :href="item.href" 
                :class="[item.current ? 'current' : '']" 
            >
            {{ item.name }}
        </a>
        </nav>
    </header>
</template>
  
<script setup>
    const navigation = [
        { name: 'Home',       current: true,     href: 'javascript:void(0)'},
        { name: 'Yggdrasil',  current: false,    href: 'https://skin.qianyiovo.com/auth/register'},
        { name: 'Discord',    current: false,    href: 'https://discord.gg/Yd7sxzAeQv'},
        { name: 'Settings',   current: false,    href: 'javascript:alert("沒有寫捏")'},
    ]
</script>

<style scoped>
    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;

        -webkit-backdrop-filter: blur(15px);
        backdrop-filter: blur(15px);

        background-color: rgba(31, 31, 31, 0.75);
        padding: 15px 0;
        color: #f8f8ff;
    }

    span.title {
        margin-left: 15px;
        letter-spacing: 2px;
        opacity: 0;
        transition: opacity,letter-spacing ease 0.55s;
    }
    nav.menu {
        opacity: 0;
        transition: opacity ease 0.35s;
        margin-right: 15px;
        float: right;
    }

    body.loaded span.title {
        letter-spacing: 0px;
        opacity: 1;
    }
    body.loaded nav.menu {
        opacity: 1;
    }

    nav.menu > a:not(:last-child) {
        margin-right: 10px;
    }
    nav.menu > a {
        color: #f8f8f8;
        text-decoration: none;
        display: inline-block;
    }
    nav.menu > a::after {
        content: "";
        width: 0px;
        height: 1px;
        display: block;
        background: #f8f8ff;
        margin: 0 0 0 auto;

        -webkit-transition: width 0.3s ease;
        transition: width 0.3s ease;
    }
    nav.menu > a:hover::after {
        width: 100%;
        margin: 0 auto 0 0;
    }

    nav.menu > a.current {
        margin-bottom: -10px;
    }
    nav.menu > a.current::after {
        position: relative;
        top: -10px;
        left: 5px;
        z-index: -1;

        width: 100%;
        height: 10px;
        border-radius: 5px;
        opacity: .35;
        background-color: #00ffff;
    }
    nav.menu > a.current:hover::after {
        -webkit-animation: shake 0.3s ease;
        animation: shake .45s linear;
    }

    @-webkit-keyframes shake {
        0%, 100% {
            -webkit-transform: translateX(0px);
        }
        33% {
            -webkit-transform: translateX(-1px);
        }
        66% {
            -webkit-transform: translateX(1px);
        }
    }
    @keyframes shake {
        0%, 100% {
            transform: translateX(0px);
        }
        33% {
            transform: translateX(-1px);
        }
        66% {
            transform: translateX(1px);
        }
    }


    @media (max-width: 600px)  {
        header {
            text-align: center;
        }
        span.title, nav.menu {
            display: block;
            width: 100%;
            float: none;
        }
        span.title {
            margin-left: 0;
        }
        nav.menu {
            margin-right: 0;
            margin-top: 5px;
        }
    }

</style>
