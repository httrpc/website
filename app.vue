<template>
  <div class="font-sans bg-gradient-to-b from-gray-50 to-white min-h-screen">
    <!-- Header/Nav Placeholder (Can be expanded later) -->
    <header class="py-4 px-6 sticky top-0 bg-white/80 backdrop-blur-md shadow-sm z-10">
      <div class="max-w-6xl mx-auto flex justify-between items-center">
        <div class="text-2xl font-bold text-gray-800">HTTRPC</div>
        <nav class="space-x-4">
          <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
          <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-gray-900">GitHub</a>
          <!-- Add link to actual docs later -->
          <a href="#" class="text-gray-600 hover:text-gray-900">Docs</a>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="py-20 px-6 text-center bg-gradient-to-r from-blue-50 to-indigo-50">
      <div class="max-w-3xl mx-auto">
        <h1 class="text-5xl md:text-6xl font-extrabold mb-4 text-gray-900 leading-tight">
          Type-Safe APIs, <span class="text-indigo-600">Any Language</span>.
        </h1>
        <p class="text-xl md:text-2xl text-gray-600 mb-8">
          Effortlessly connect frontends to backends with HTTRPC. Enjoy end-to-end type safety like tRPC, but across your entire stack, regardless of language.
        </p>
        <div class="space-x-4">
          <a href="#getting-started" class="bg-indigo-600 hover:bg-indigo-700 text-white font-semibold py-3 px-6 rounded-lg shadow-md transition duration-200">
            Get Started
          </a>
          <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="bg-white hover:bg-gray-100 text-gray-700 font-semibold py-3 px-6 rounded-lg border border-gray-300 shadow-sm transition duration-200">
            View on GitHub
          </a>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-16 px-6">
      <div class="max-w-6xl mx-auto">
        <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-gray-800">Why HTTRPC?</h2>
        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          <!-- Feature 1: Type Safety -->
          <div class="bg-white p-6 rounded-lg shadow-lg border border-gray-100 text-center">
            <div class="i-carbon-checkmark-shield text-4xl text-indigo-500 mx-auto mb-4"></div>
            <h3 class="text-xl font-semibold mb-2 text-gray-800">End-to-End Type Safety</h3>
            <p class="text-gray-600">Leverage JSON Schema for robust type validation between client and server.</p>
          </div>
          <!-- Feature 2: Language Agnostic -->
          <div class="bg-white p-6 rounded-lg shadow-lg border border-gray-100 text-center">
            <div class="i-carbon-language text-4xl text-indigo-500 mx-auto mb-4"></div>
            <h3 class="text-xl font-semibold mb-2 text-gray-800">Truly Language Agnostic</h3>
            <p class="text-gray-600">Integrate seamlessly with any backend or frontend via standard HTTP.</p>
          </div>
          <!-- Feature 3: Simple Integration -->
          <div class="bg-white p-6 rounded-lg shadow-lg border border-gray-100 text-center">
            <div class="i-carbon-plug text-4xl text-indigo-500 mx-auto mb-4"></div>
            <h3 class="text-xl font-semibold mb-2 text-gray-800">Simple Integration</h3>
            <p class="text-gray-600">Easy to adopt with minimal boilerplate. Focus on your logic, not the plumbing.</p>
          </div>
          <!-- Feature 4: Flexible Patterns -->
          <div class="bg-white p-6 rounded-lg shadow-lg border border-gray-100 text-center">
            <div class="i-carbon-flow-connection text-4xl text-indigo-500 mx-auto mb-4"></div>
            <h3 class="text-xl font-semibold mb-2 text-gray-800">Flexible Interaction</h3>
            <p class="text-gray-600">Supports Queries, Mutations, and Subscriptions (via SSE) out of the box.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- How it Works / Core Concept -->
     <section class="py-16 px-6 bg-gray-100">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-800">Simple & Standard</h2>
        <p class="text-lg text-gray-600 mb-8">
          HTTRPC uses standard HTTP methods and headers. Define your API contract with JSON Schema, and you're ready to go. No complex code generation steps required.
        </p>
        <pre class="bg-gray-800 text-left p-4 rounded-lg overflow-x-auto text-sm shadow-lg"><code class="language-http font-mono text-gray-300"><span class="text-green-400">POST /httrpc/users/createUser</span>
<span class="text-cyan-400">X-HTTRPC-Version:</span> <span class="text-yellow-400">1</span>
<span class="text-cyan-400">Content-Type:</span> <span class="text-yellow-400">application/json</span>
<span class="text-cyan-400">Authorization:</span> <span class="text-yellow-400">Bearer YOUR_TOKEN_HERE</span>

<span class="text-purple-400">{</span>
  <span class="text-blue-400">"type"</span><span class="text-gray-300">:</span> <span class="text-orange-400">"named"</span><span class="text-gray-300">,</span>
  <span class="text-blue-400">"args"</span><span class="text-gray-300">: {</span>
    <span class="text-blue-400">"name"</span><span class="text-gray-300">:</span> <span class="text-orange-400">"Jane Smith"</span><span class="text-gray-300">,</span>
    <span class="text-blue-400">"email"</span><span class="text-gray-300">:</span> <span class="text-orange-400">"jane@example.com"</span>
  <span class="text-gray-300">}</span>
<span class="text-purple-400">}</span></code></pre>
      </div>
    </section>

    <!-- Getting Started / CTA -->
    <section id="getting-started" class="py-20 px-6 text-center">
       <div class="max-w-3xl mx-auto">
        <h2 class="text-3xl md:text-4xl font-bold mb-6 text-gray-800">Ready to Simplify Your APIs?</h2>
        <p class="text-lg text-gray-600 mb-8">
          Explore the documentation, check out examples, or dive straight into the code on GitHub.
        </p>
        <div class="space-x-4">
           <a href="#" class="bg-indigo-600 hover:bg-indigo-700 text-white font-semibold py-3 px-6 rounded-lg shadow-md transition duration-200">
            Read the Docs
          </a>
          <a href="https://github.com/httrpc/httrpc/tree/main/examples" target="_blank" rel="noopener noreferrer" class="bg-white hover:bg-gray-100 text-gray-700 font-semibold py-3 px-6 rounded-lg border border-gray-300 shadow-sm transition duration-200">
            View Examples
          </a>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="mt-12 py-8 px-6 border-t border-gray-200 bg-gray-100">
      <div class="max-w-6xl mx-auto text-center text-gray-500 text-sm">
        <p class="mb-2">HTTRPC Framework - Licensed under MIT</p>
        <p>
          <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="hover:text-gray-800">GitHub</a> |
          <a href="#" class="hover:text-gray-800">Documentation</a> |
          <a href="./SPEC.md" class="hover:text-gray-800">Specification</a>
        </p>
      </div>
    </footer>

  </div>
</template>

<style>
/* Using UnoCSS reset and utilities, minimal global styles needed */
body {
  @apply antialiased; /* Improves font rendering */
}

/* Add styles for syntax highlighting in <pre> tags if needed */
/* Example: You might integrate Prism.js or similar and style here */
</style>
