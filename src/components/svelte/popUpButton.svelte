<script lang="ts">
    import { onMount } from 'svelte';

    export let link: string;
    export let buttonText: string;
    let modal: any;
    // let overlay: any;

    onMount(() => {
        modal = document.querySelector('.modal');
        // overlay = document.querySelector('.overlay');
    });

    const openModal = function () {
        if (modal) {
            modal.classList.remove('hidden');
            // overlay.classList.remove('hidden');
        }
    };

    const closeModal = function () {
        if (modal) {
            modal.classList.add('hidden');
            // overlay.classList.add('hidden');
        }
    };
</script>

<section class="modal hidden fixed inset-0 flex items-center justify-center z-10">
    <div class="flex flex-col gap-2 w-[85vw] h-[85vh] p-5 min-h-60 bg-[#f0eab5] text-black rounded-lg">
        <div class="flex flex-col items-center justify-between">
            <div class="flex flex-row gap-5">
            <button class="btn btn-close p-3 rounded-full bg-black z-20 text-white" on:click={closeModal}>Close</button>
            <a href={link.replace('/hidden','')} class="btn btn-open p-3 rounded-full bg-black z-20 text-white">Go To Page</a>
            </div>
            <iframe src={link} frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" title="frame" allowfullscreen class="w-full h-[75vh]"></iframe>
    </div>
</section>

<button class="btn btn-open bottom-4 right-4 text-white bg-green-600 p-2 rounded-md mt-3 inline-block" on:click={openModal}>{buttonText}</button>
<style>
    /* BEGIN: Tailwind CSS */
    @import 'tailwindcss/base';
    @import 'tailwindcss/components';
    @import 'tailwindcss/utilities';
    /* END: Tailwind CSS */

    /* Additional custom styles */
    .hidden {
        display: none;
    }
</style>