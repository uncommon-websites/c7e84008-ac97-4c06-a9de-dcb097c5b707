<script>
  export let mobileMenuOpen = false;
</script>

<nav class="flex items-center justify-between px-6 py-4 max-w-[1400px] mx-auto w-full text-sm font-medium text-gray-600">
  <div class="flex items-center gap-8">
    <a href="/" class="text-black font-bold text-lg tracking-tight flex items-center gap-1">
      <!-- Simple representation of the ElevenLabs logo mark if needed, or just text -->
      <span>IIElevenLabs</span>
    </a>
    
    <div class="hidden lg:flex items-center gap-6">
      <button class="hover:text-black flex items-center gap-1">Creative Platform <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Agents Platform <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Developers <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <button class="hover:text-black flex items-center gap-1">Resources <svg width="10" height="6" viewBox="0 0 10 6" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M1 1L5 5L9 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></button>
      <a href="/enterprise" class="hover:text-black">Enterprise</a>
      <a href="/pricing" class="hover:text-black">Pricing</a>
    </div>
  </div>

  <div class="flex items-center gap-4">
    <a href="/login" class="hover:text-black hidden sm:block">Log In</a>
    <a href="/signup" class="bg-black text-white px-4 py-2 rounded-full hover:bg-gray-800 transition-colors text-xs font-semibold">Sign Up</a>
    <button class="lg:hidden" on:click={() => mobileMenuOpen = !mobileMenuOpen}>
        Menu
    </button>
  </div>
</nav>
