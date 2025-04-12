<template>
    <section class="text-white mt-20" id="contact">
        <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Let's Connect</h2>
        <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
            <div>
                <p class="text-[#adb7be]"></p>
                <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/metro/50/ffffff/new-post.png" alt="new-post" class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>Email</h4>
                            <p>ln@lucaneumann.com</p>
                        </div>
                    </div>
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/?size=100&id=7880&format=png&color=ffffff" alt="location" class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>Location</h4>
                            <p>Tyrol, Austria</p>
                        </div>
                    </div>
                    <div class="flex mb-10 items-center">
                        <div class="p-2"
                            style="background: #111a3e; width: 50px;height: 46px; display: flex;justify-content: center; border-radius: 50%;
                        overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
                            <img src="https://img.icons8.com/ios-filled/50/ffffff/linkedin.png" alt="linkedin"
                                class="w-6">
                        </div>
                        <div class="ml-5 text-white">
                            <h4>LinkedIn</h4>
                            <p>www.linkedin.com/in/lucaneumann/</p>
                        </div>
                    </div>
                </div>
            </div>
            <div
            style="background: #111a3e; width: 100%;height: 100%; border-radius: 20px;
            overflow: hidden;border: 1px solid #111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
            <h2 class="text-4xl font-bold text-white mb-4 pt-4 text-center">Message
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">Luca</span>
                </h2>
            <form class="flex flex-col p-2" data-aos="zoom-in-up" id="myForm" action="https://formspree.io/f/xoqyyolb" method="POST">
                <div class="mb-6">
                    <!--<label for="name" class="text-white block mb-2 text-sm font-medium">name</label> -->
                    <input type="text" id="name" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Name" name="Name:">
                </div>
                <div class="mb-6">
                    <!--<label for="email" class="text-white block mb-2 text-sm font-medium">email</label> -->
                    <input type="email" id="email" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Email" name="Email:">
                </div>
                <div class="mb-6">
                    <!-- <label for="subject" class="text-white block mb-2 text-sm font-medium">Subject</label> -->
                    <input type="text" id="subject" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Subject" name="Subject:">
                </div>
                <div class="mb-6">
                    <!-- <label for="message" class="text-white block mb-2 text-sm font-medium">Message</label> -->
                    <textarea id="body" class="bg-[#111827] placeholder:[#9CA2A9] text-gray-100 text-sm rounded-lg block w-full p-2.5"
                    placeholder="Message... " name="Message:"></textarea>
                </div>
                <button class="z-1 w-[100%!important] px-6 md:px-7 py-3 rounded-full sm:w-max flex justify-center text-white bg-primary border-2 border-transparent mb-4" id="submit" value="send" type="submit">
                    Send Message
                </button>
            </form>
        </div>
        <div class="bg-gradient-to-tr opacity-25 from-[#570cac] to-primary blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 
        -translate-1/2
        "></div>
        </div>
    </section>
</template>
<script>

</script>
