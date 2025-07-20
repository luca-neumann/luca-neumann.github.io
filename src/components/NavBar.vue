<template>
    <header class="flex justify-between items-center p-6 bg-opacity-30 bg-[#111827] relative z-20">
        <div class="text-white text-3xl font-bold">
            <img src="@/assets/LN-Profile-white.png" alt="LN" width="60px" height="60px">
        </div>
        <!-- Mobile Toggle Button -->
        <div class="md:hidden z-30">
            <button type="button" 
            class="block focus:outline-none"
            @click="isMenuOpen = !isMenuOpen"
            >
                <span v-if="isMenuOpen" class="text-5xl">
                    <img src="https://img.icons8.com/ios-filled/100/ffffff/delete-sign.png" alt="close" width="50" height="50">
                </span>
                <span v-else class="text-5xl">
                    <img src="https://img.icons8.com/ios-filled/100/ffffff/menu--v6.png" alt="menu" width="50" height="50">
                </span>
            </button>
        </div>
        <!-- Navbar Link -->
        <nav
        :class="['fixed inset-0 z-20 flex flex-col items-center justify-center bg-[#111827] md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
            isMenuOpen ? 'block':'hidden'
        ]"
        >
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a :href="item.href" 
                    class="block text-white transition hover:text-primary ease-linear text-2xl md:text-lg"
                    @click="scrollToSection(item.href)"
                    >
                        {{ item.name }}
                    </a>
                </li>
            </ul>
        </nav>
    </header>
</template>
<script setup>
import { ref, onMounted } from 'vue';
const Menu =ref([
    //{name:'Services',href:'#services'},
    {name:'About',href:'#about'},
    {name:'Skills',href:'#skills'},
    {name:'News',href:'#news'},
    //{name:'Testimonials',href:'#testimonials'},
    {name:'Contact',href:'#contact'},
]);

const isMenuOpen =ref(false)
const scrollToSection =(href)=>{
    isMenuOpen.value=false;
    const section=document.querySelector(href);
    if(section){
        section.scrollIntoView({behavior :'smooth'});
    }

}

// JSON-LD Script in Head hinzufügen
onMounted(() => {
     if (!document.querySelector('script[type="application/ld+json"]')) {
        const script = document.createElement('script');
        script.type = 'application/ld+json';
        script.text = JSON.stringify({
            '@context': 'https://schema.org',
            '@type': 'Person',
            name: 'Luca Neumann',
            url: 'https://lucaneumann.com',
            sameAs: [
            'https://www.linkedin.com/in/lucaneumann/',
            'https://www.instagram.com/_lucaneumann_/',
            ],
            alumniOf: {
            '@type': 'EducationalOrganization',
            name: 'HTL Anichstraße',
            url: 'https://htlinn.ac.at/',
            },
            affiliation: {
            '@type': 'Organization',
            name: 'AlpenPro Junior Company',
            },
            jobTitle: 'Student',
            worksFor: {
            '@type': 'CollegeOrUniversity',
            name: 'WU Vienna – Vienna University of Economics and Business',
            url: 'https://www.wu.ac.at',
            },
        });
        document.head.appendChild(script);
    }
});
</script>
