<template>
 <!-- Header -->
 <!-- <div class="fixed w-full flex items-center justify-between  top-0 text-white z-10">
        <div class="flex items-center justify-start md:justify-center pl-3 w-14 md:w-64 h-14 bg-slate-600 border-none">
          <img class="w-7 h-7 md:w-10 md:h-10 mr-2 rounded-full overflow-hidden" src="https://therminic2018.eu/wp-content/uploads/2018/07/dummy-avatar.jpg" />
          <span class="hidden md:block">ADMIN</span>
        </div>
        <div class="flex justify-between items-center h-20 bg-slate-800 header-right">
          <div class="bg-white rounded flex items-center w-80 max-w-2xl mr-4  m-6 p-2 shadow-sm border border-gray-200">
            <button class="outline-none focus:outline-none">
              <svg class="w-5 text-gray-600 h-5 cursor-pointer" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" stroke="currentColor" viewBox="0 0 24 24"><path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg>
            </button>
            <input type="search" name="" id="" placeholder="Search" class="px-20  pl-6 text-sm text-black outline-none focus:outline-none bg-transparent" />
          </div>
          <ul class="flex items-center">
            
            <li>
              <div class="block w-px h-6 mx-3 bg-gray-400 dark:bg-gray-700"></div>
            </li>
            <li>
              <a href="#" class="flex items-center mr-4 font-bold text-md text-orange-600">
                <span class="inline-flex mr-1">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"></path></svg>
                </span>
                Logout
              </a>
            </li>
          </ul>
        </div>
      </div>  -->
      <!-- ./Header -->
    
      <!-- Sidebar -->
       <!-- <div class="fixed flex flex-col  top-0 left-0 w-14 hover:w-64 md:w-64 bg-slate-900 h-full text-white transition-all duration-300 border-none z-10 sidebar">
        <div class="overflow-y-auto overflow-x-hidden flex flex-col justify-between flex-grow">
          <ul class="flex flex-col py-4 space-y-1">
            <li class="px-5 hidden md:block">
              <div class="flex flex-row items-center h-4">
                <div class="text-md font-bold    text-orange-600 uppercase">Learn with the best</div>
              </div>
            </li>
            <li>
              <a href="/" class=" rounded-md relative flex flex-row items-center h-11  hover:bg-orange-600  text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500  pr-6">
                <span class="inline-flex justify-center items-center ml-4">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
                </span>
                <span class="ml-2 text-sm tracking-wide truncate">Home</span>
              </a>
            </li>
            <li>
              <div class=" ">
    <div class="relative   ml-6 flex flex-row items-center h-11  pr-0 ">
        <button  class=" inline-flex justify-center items-center  ">
            <span class="select-none p-2 text-lg font-bold font-mono text-orange-600">COURSES</span> 
        </button>
         </div>
    </div>
            </li>
            <li>
              <div class=" ">
                <div class="relative rounded-md  ml-3 flex flex-row items-center h-11 hover:bg-orange-600  text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-600 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Data science</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Cyber security</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Data mining</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Deep learning</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Artificial intelligence</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Computer science</span>     
        </button>
        </div>
        <div class="relative rounded-md  ml-3 flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-500 pr-0 ">
        <button  class=" inline-flex justify-center items-center">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
            <span class="select-none p-2 text-sm">Big data</span>     
        </button>
        </div>
</div>
                   
               
              
            </li>
            
            
            <li class="px-5 hidden md:block">
              <div class="flex flex-row items-center mt-5 h-8">
                <div class="text-sm  font-bold p-2 text-orange-600 uppercase">Settings</div>
              </div>
            </li>
            <li>
              <a href="#" class="relative rounded-md flex flex-row items-center h-11  hover:bg-orange-600  text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-600  pr-6">
                <span class="inline-flex justify-center items-center ml-4">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
                </span>
                <span class="ml-2 text-sm tracking-wide truncate">Profile</span>
              </a>
            </li>
            <li>
              <a href="#" class="relative rounded-md flex flex-row items-center h-11  hover:bg-orange-600 dark:hover:bg-gray-600 text-white-600 hover:text-white-800 border-l-4 border-transparent hover:border-slate-600  pr-6">
                <span class="inline-flex justify-center items-center ml-4">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path>
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                  </svg>
                </span>
                <span class="ml-2 text-sm tracking-wide truncate">Settings</span>
              </a>
            </li>
          </ul>
          <p class="mb-14 px-5 py-3 hidden md:block text-center  text-orange-600 text-xs">Copyright @2023</p>
        </div>
      </div>  -->
      <!-- ./Sidebar -->







  <div>
    <NuxtPage/>
  </div>
</template>
