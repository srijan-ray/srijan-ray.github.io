<script setup lang="ts">
function downloadPDF() {
  const link = document.createElement('a');
  link.href = '../../public/SrijanRayResume.pdf';  
  link.download = 'SrijanRayResume.pdf';
  link.click();
  console.log("here");
}
</script>
<template>
    <div class="navbar bg-base-200 sticky top-0 z-50">
        <div class="flex-1">
            <a href="/" class="btn btn-ghost text-xl">Srijan Ray</a>
        </div>
        <div class="flex-none">
            <div class="dropdown dropdown-end">
                <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24"
                        stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16"
                            transform="scale (-1, 1)" transform-origin="center" />
                    </svg>
                </div>
                <ul tabindex="0"
                    class="menu menu-sm dropdown-content bg-base-200 rounded-box z-[1] mt-3 w-52 p-2 shadow">
                    <li>
                        <a href="/about">
                            About
                        </a>
                    </li>
                    <li>
                        <a href="/research">
                            Research
                        </a>
                    </li>
                    <li>
                        <a href="/projects">
                            Projects
                        </a>
                    </li>
                    <li>
                        <button @click="downloadPDF">
                                Resume/CV
                        </button>
                    </li>
                    <li>
                        <a href="/blog">
                            Blog
                        </a>
                    </li>
                </ul>
            </div>
            <div class="hidden lg:flex">
                <ul class="menu menu-horizontal px-1 -mt-3">
                    <li>
                        <a role="button" href="/about" class="btn btn-outline btn-sm mx-2">
                            About
                        </a>
                    </li>
                    <li>
                        <a role="button" href="/research" class="btn btn-outline btn-sm mx-2">
                            Research
                        </a>
                    </li>
                    <li>
                        <a role="button" href="/projects" class="btn btn-outline btn-sm mx-2">
                            Projects
                        </a>
                    </li>
                    <li>
                        <a role="button" class="btn btn-outline btn-sm mx-2" download="SrijanRayResume" href="../../public/SrijanRayResume.pdf">
                            Resume/CV
                        </a>
                    </li>
                    <li>
                        <a role="button" href="/blog" class="btn btn-outline btn-sm mx-2">
                            Blog
                        </a>
                    </li>
                    <a href="https://linkedin.com/in/srijan-ray" target="_blank" rel="noopener noreferrer" role="button"
                        class="btn btn-square mx-1 -mt-1">
                        <button class="text-xl btn btn-square">
                            <svg width="25" height="25" viewBox="0 0 15 15" fill="none"
                                xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M2 1C1.44772 1 1 1.44772 1 2V13C1 13.5523 1.44772 14 2 14H13C13.5523 14 14 13.5523 14 13V2C14 1.44772 13.5523 1 13 1H2ZM3.05 6H4.95V12H3.05V6ZM5.075 4.005C5.075 4.59871 4.59371 5.08 4 5.08C3.4063 5.08 2.925 4.59871 2.925 4.005C2.925 3.41129 3.4063 2.93 4 2.93C4.59371 2.93 5.075 3.41129 5.075 4.005ZM12 8.35713C12 6.55208 10.8334 5.85033 9.67449 5.85033C9.29502 5.83163 8.91721 5.91119 8.57874 6.08107C8.32172 6.21007 8.05265 6.50523 7.84516 7.01853H7.79179V6.00044H6V12.0047H7.90616V8.8112C7.8786 8.48413 7.98327 8.06142 8.19741 7.80987C8.41156 7.55832 8.71789 7.49825 8.95015 7.46774H9.02258C9.62874 7.46774 10.0786 7.84301 10.0786 8.78868V12.0047H11.9847L12 8.35713Z"
                                    fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path>
                            </svg>
                        </button>
                    </a>
                    <a href="https://github.com/StrontiumComputer" target="_blank" rel="noopener noreferrer"
                        role="button" class="btn btn-square mx-1 -mt-1">
                        <button class="text-xl btn btn-square">
                            <svg width="25" height="25" viewBox="0 0 15 15" fill="none"
                                xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M7.49933 0.25C3.49635 0.25 0.25 3.49593 0.25 7.50024C0.25 10.703 2.32715 13.4206 5.2081 14.3797C5.57084 14.446 5.70302 14.2222 5.70302 14.0299C5.70302 13.8576 5.69679 13.4019 5.69323 12.797C3.67661 13.235 3.25112 11.825 3.25112 11.825C2.92132 10.9874 2.44599 10.7644 2.44599 10.7644C1.78773 10.3149 2.49584 10.3238 2.49584 10.3238C3.22353 10.375 3.60629 11.0711 3.60629 11.0711C4.25298 12.1788 5.30335 11.8588 5.71638 11.6732C5.78225 11.205 5.96962 10.8854 6.17658 10.7043C4.56675 10.5209 2.87415 9.89918 2.87415 7.12104C2.87415 6.32925 3.15677 5.68257 3.62053 5.17563C3.54576 4.99226 3.29697 4.25521 3.69174 3.25691C3.69174 3.25691 4.30015 3.06196 5.68522 3.99973C6.26337 3.83906 6.8838 3.75895 7.50022 3.75583C8.1162 3.75895 8.73619 3.83906 9.31523 3.99973C10.6994 3.06196 11.3069 3.25691 11.3069 3.25691C11.7026 4.25521 11.4538 4.99226 11.3795 5.17563C11.8441 5.68257 12.1245 6.32925 12.1245 7.12104C12.1245 9.9063 10.4292 10.5192 8.81452 10.6985C9.07444 10.9224 9.30633 11.3648 9.30633 12.0413C9.30633 13.0102 9.29742 13.7922 9.29742 14.0299C9.29742 14.2239 9.42828 14.4496 9.79591 14.3788C12.6746 13.4179 14.75 10.7025 14.75 7.50024C14.75 3.49593 11.5036 0.25 7.49933 0.25Z"
                                    fill="currentColor" fill-rule="evenodd" clip-rule="evenodd"></path>
                            </svg>
                        </button>
                    </a>
                    <a>
                        <label class="mx-2 pt-[0.1rem] swap swap-rotate">
                            <!-- this hidden checkbox controls the state -->
                            <input type="checkbox" class="theme-controller" value="dark" />

                            <!-- sun icon -->
                            <svg class="swap-off h-8 w-8 fill-current" xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 24 24">
                                <path
                                    d="M5.64,17l-.71.71a1,1,0,0,0,0,1.41,1,1,0,0,0,1.41,0l.71-.71A1,1,0,0,0,5.64,17ZM5,12a1,1,0,0,0-1-1H3a1,1,0,0,0,0,2H4A1,1,0,0,0,5,12Zm7-7a1,1,0,0,0,1-1V3a1,1,0,0,0-2,0V4A1,1,0,0,0,12,5ZM5.64,7.05a1,1,0,0,0,.7.29,1,1,0,0,0,.71-.29,1,1,0,0,0,0-1.41l-.71-.71A1,1,0,0,0,4.93,6.34Zm12,.29a1,1,0,0,0,.7-.29l.71-.71a1,1,0,1,0-1.41-1.41L17,5.64a1,1,0,0,0,0,1.41A1,1,0,0,0,17.66,7.34ZM21,11H20a1,1,0,0,0,0,2h1a1,1,0,0,0,0-2Zm-9,8a1,1,0,0,0-1,1v1a1,1,0,0,0,2,0V20A1,1,0,0,0,12,19ZM18.36,17A1,1,0,0,0,17,18.36l.71.71a1,1,0,0,0,1.41,0,1,1,0,0,0,0-1.41ZM12,6.5A5.5,5.5,0,1,0,17.5,12,5.51,5.51,0,0,0,12,6.5Zm0,9A3.5,3.5,0,1,1,15.5,12,3.5,3.5,0,0,1,12,15.5Z" />
                            </svg>

                            <!-- moon icon -->
                            <svg class="swap-on h-8 w-8 fill-current" xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 24 24">
                                <path
                                    d="M21.64,13a1,1,0,0,0-1.05-.14,8.05,8.05,0,0,1-3.37.73A8.15,8.15,0,0,1,9.08,5.49a8.59,8.59,0,0,1,.25-2A1,1,0,0,0,8,2.36,10.14,10.14,0,1,0,22,14.05,1,1,0,0,0,21.64,13Zm-9.5,6.69A8.14,8.14,0,0,1,7.08,5.22v.27A10.15,10.15,0,0,0,17.22,15.63a9.79,9.79,0,0,0,2.1-.22A8.11,8.11,0,0,1,12.14,19.73Z" />
                            </svg>
                        </label>
                    </a>
                </ul>
            </div>
        </div>
    </div>
</template>
