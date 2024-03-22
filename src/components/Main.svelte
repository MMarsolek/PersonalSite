<script>
import Step from "./Step.svelte"

const steps = [
    {name:"Auction House" , icon:"fa-solid fa-gavel"},
    {name:"Street Fighter" , icon:"fa-solid fa-gamepad"},
    {name:"SkyFall-Travel" , icon:"fa-solid fa-plane"},
]
const benefits = [
    {name: "a self taught", description:"In early 2020, I decided to throw myself fully into learning programming from home. This meant taking many free courses and following different tutorials online. I was lucky enough to be able to attend an official coding boot camp in 2021 before offically joining the work force. "},
    {name: "an enthusiastic learner", description:"My goal is to contribute to cutting-edge web and application projects, continuously improve my abilities, and positively impact the user's digital experience. That means I must constantly be up to learning new skills and expanding my knowledge. It is important to remember that there is always room for growth."},
    {name: "an excellent communicator", description:"My many teaching and customer facing roles have lead me to become an excellent communicator. I have seen first hand how important good communication is between coworks and other teams."},
]
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left md:gap-8 lg:gap 10">
            <h2 class="font-semibold text-4xl sm:text5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Mariah</span> Marsolek
                <br/> Full Stack
                <span class="poppins text-violet-400"> Developer</span> 
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite languages</span> include TypeScript, JavaScript, Java, and Go! 
            </p>
            <a href="https://www.linkedin.com/in/mariahmarsolek" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-cl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">        
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">
                    Get in touch &rarr;
                </h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center ">
            <img src={"/assets/images/profile.png"} alt="profile of Mariah" class="object-cover z-[2] max-h-[70vh]"/>
        </div>
    </section>


    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text:4xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a href="https://github.com/MMarsolek" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
            <i class="fa-brands fa-github"/>
        </a>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Auction House is an auction site that allows users to place bids on items. This project was created using <strong class="text-violet-400">GO</strong> and <strong class="text-violet-400">React</strong>. </p>
            </Step>
            <Step step={steps[1]}>
                <p>This project serves as the backend for a Street Fighter combo translator. The backend of this project was created using <strong class="text-violet-400">JavaScript</strong></p>
            </Step>
            <Step step={steps[2]}>
                <p>This project allows a user to create, view, edit, and delete future travel plans. This project was created using <strong class="text-violet-400">JavaScript</strong>, <strong class="text-violet-400">CSS (JASS)</strong>, and <strong class="text-violet-400">SQL</strong></p>
            </Step>
        </div>
    </section>
    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-24 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . . 
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>
                            {benefit.description}
                        </p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-violet-400 poppins">Complete</span> package
        </h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th/>
                        <th class="whitespace-nowrap p-2 px-4"> Candidate #1 </th>
                        <th class="whitespace-nowrap p-2 px-4"> Candidate #2 </th>
                        <th class="whitespace-nowrap p-2 px-4"> Candidate #3 </th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8"> Me </th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="boder-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Dedication</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-green-500"></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="boder-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Critical Thought</td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-green-500"></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="boder-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Interpersonal Skills</td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-green-500"></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="boder-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap">Programming Ability</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-slate-500"></td>
                        <td><i class="fa-solid fa-check text-green-500"></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50 ">
            <p>
                Scroll to see more &rarr;
            </p>
        </div>
        <p class="mx-auto">
            So why not invest?
        </p>
    </section>
</main>