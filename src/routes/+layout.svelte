<script>
  import Footer from '$lib/components/Layout/Footer.svelte';
  import Header from '$lib/components/Layout/Header.svelte';
  import '../app.css';
</script>

<div class="app 2xl:text-[20px] bg-[#F8F9FE]">
  <!-- Top Bar -->
  <div class="w-full py-2 h-10 bg-[#0FC1A7]"></div>
  
  <!-- Header -->
  <header>
    <Header />
  </header>
  
  <!-- Main Content -->
  <main class="antialiased text-default bg-page tracking-tight">
    <slot />
  </main>
  
  <!-- Footer -->
  <footer>
    <Footer />
  </footer>
</div>
