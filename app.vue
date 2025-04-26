<template>
  <div class="font-sans min-h-screen bg-gradient-to-b from-navy-950 to-indigo-950 text-white overflow-hidden">
    <!-- Ambient Background Elements -->
    <div class="fixed inset-0 z-0">
      <!-- Animated gradient mesh -->
      <div class="absolute inset-0 opacity-10 bg-[radial-gradient(ellipse_at_top_right,_var(--tw-gradient-stops))] from-blue-400 via-indigo-500 to-purple-800"></div>
      <!-- Grid pattern -->
      <div class="absolute inset-0 bg-grid-pattern opacity-5"></div>
    </div>

    <!-- Main Content -->
    <div class="relative z-10">
      <!-- Header/Nav -->
      <header class="sticky top-0 backdrop-blur-xl bg-navy-900/30 border-b border-white/5 z-50">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
          <a href="#" class="text-2xl font-bold text-white">HTTRPC</a>
          <nav class="flex items-center space-x-8">
            <a href="#features" class="text-slate-300 hover:text-white transition-colors duration-200">Features</a>
            <a href="#code" class="text-slate-300 hover:text-white transition-colors duration-200">Code</a>
            <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="text-slate-300 hover:text-white transition-colors duration-200">GitHub</a>
            <a href="#" class="px-5 py-2 rounded-full bg-white/10 hover:bg-white/15 text-white font-medium transition-all duration-200">
              Docs
            </a>
          </nav>
        </div>
      </header>

      <!-- Hero Section -->
      <section class="py-32 px-6 relative overflow-hidden">
        <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
          <!-- Text content -->
          <div class="space-y-8">
            <h1 class="text-5xl md:text-7xl font-extrabold leading-tight">
              <span class="block text-white">Type-Safe APIs.</span>
              <span class="block mt-2 bg-clip-text text-transparent bg-gradient-to-r from-cyan-400 to-blue-500 pb-4">
                Any Language.
              </span>
            </h1>
            <p class="text-xl text-slate-300 leading-relaxed">
              Connect frontends to backends with confidence. HTTRPC delivers end-to-end type safety across your entire stack, regardless of language.
            </p>
            <div class="flex flex-wrap gap-5 pt-4">
              <a href="#getting-started" class="flex items-center px-6 py-3 bg-gradient-to-r from-blue-500 to-indigo-600 hover:from-blue-600 hover:to-indigo-700 text-white font-medium rounded-full transition-all duration-200">
                <span>Get Started</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L12.586 11H5a1 1 0 110-2h7.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
              </a>
              <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="flex items-center px-6 py-3 bg-white/10 hover:bg-white/15 text-white font-medium rounded-full transition-all duration-200">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
                <span>GitHub</span>
              </a>
            </div>
          </div>
          
          <!-- Code example -->
          <div class="code-container">
            <pre class="text-left p-6 rounded-xl bg-navy-900/80 border border-indigo-800/30 overflow-x-auto text-sm shadow-lg"><code class="language-typescript font-mono">
<span class="text-pink-400">import</span> <span class="text-cyan-300">{ createClient }</span> <span class="text-pink-400">from</span> <span class="text-green-400">'httrpc'</span>;

<span class="text-slate-500">// Type-safe client</span>
<span class="text-pink-400">const</span> <span class="text-cyan-300">client</span> = <span class="text-yellow-400">createClient</span>({
  <span class="text-purple-400">baseUrl:</span> <span class="text-green-400">'https://api.example.com'</span>,
  <span class="text-purple-400">headers:</span> {
    <span class="text-purple-400">Authorization:</span> <span class="text-green-400">`Bearer ${token}`</span>
  }
});

<span class="text-slate-500">// Fully typed response</span>
<span class="text-pink-400">const</span> <span class="text-cyan-300">user</span> = <span class="text-pink-400">await</span> client.users.getUser({
  <span class="text-purple-400">id:</span> <span class="text-orange-400">123</span>
});</code></pre>
          </div>
        </div>
      </section>

      <!-- Features Section -->
      <section id="features" class="py-32 px-6 relative">
        <div class="max-w-7xl mx-auto">
          <div class="text-center mb-20">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
              Why Choose HTTRPC?
            </h2>
            <p class="text-xl text-slate-300 max-w-3xl mx-auto">
              A modern approach to API development that prioritizes developer experience and type safety.
            </p>
          </div>
          
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            <!-- Feature 1: Type Safety -->
            <div class="feature-card">
              <div class="feature-icon bg-gradient-to-br from-purple-500 to-indigo-600 mb-6">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-white mb-3">End-to-End Type Safety</h3>
              <p class="text-slate-300">JSON Schema validation ensures robust type contracts between client and server.</p>
            </div>
            
            <!-- Feature 2: Language Agnostic -->
            <div class="feature-card">
              <div class="feature-icon bg-gradient-to-br from-cyan-500 to-blue-600 mb-6">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12.87 15.07l-2.54-2.51.03-.03c1.74-1.94 2.98-4.17 3.71-6.53H17V4h-7V2H8v2H1v1.99h11.17C11.5 7.92 10.44 9.75 9 11.35 8.07 10.32 7.3 9.19 6.69 8h-2c.73 1.63 1.73 3.17 2.98 4.56l-5.09 5.02L4 19l5-5 3.11 3.11.76-2.04zM18.5 10h-2L12 22h2l1.12-3h4.75L21 22h2l-4.5-12zm-2.62 7l1.62-4.33L19.12 17h-3.24z"/>
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-white mb-3">Language Agnostic</h3>
              <p class="text-slate-300">Integrate seamlessly with any backend or frontend using standard HTTP protocols.</p>
            </div>
            
            <!-- Feature 3: Simple Integration -->
            <div class="feature-card">
              <div class="feature-icon bg-gradient-to-br from-teal-500 to-green-600 mb-6">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M16 7v-4l8 8-8 8v-4.5c-5 0-8.5 1.5-11 5l2-8c1.5-2.5 5-4 9-4z"/>
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-white mb-3">Easy Integration</h3>
              <p class="text-slate-300">Quick adoption with minimal setup. Focus on building, not configuration.</p>
            </div>
            
            <!-- Feature 4: Flexible Patterns -->
            <div class="feature-card">
              <div class="feature-icon bg-gradient-to-br from-amber-500 to-orange-600 mb-6">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M3.9 12c0-1.71 1.39-3.1 3.1-3.1h4V7H7c-2.76 0-5 2.24-5 5s2.24 5 5 5h4v-1.9H7c-1.71 0-3.1-1.39-3.1-3.1zM8 13h8v-2H8v2zm9-6h-4v1.9h4c1.71 0 3.1 1.39 3.1 3.1s-1.39 3.1-3.1 3.1h-4V17h4c2.76 0 5-2.24 5-5s-2.24-5-5-5z"/>
                </svg>
              </div>
              <h3 class="text-xl font-semibold text-white mb-3">Flexible Interaction</h3>
              <p class="text-slate-300">Supports Queries, Mutations, and Subscriptions for diverse API needs.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Code Example Section -->
      <section id="code" class="py-32 px-6 relative">
        <div class="max-w-6xl mx-auto">
          <div class="grid md:grid-cols-2 gap-12 items-center">
            <!-- Left side: Code example -->
            <div>
              <pre class="text-left p-6 rounded-xl bg-navy-900/80 border border-indigo-800/30 overflow-x-auto text-sm shadow-lg"><code class="language-json font-mono">
<span class="text-purple-400">{</span>
  <span class="text-blue-400">"type"</span><span class="text-slate-300">:</span> <span class="text-orange-400">"named"</span><span class="text-slate-300">,</span>
  <span class="text-blue-400">"args"</span><span class="text-slate-300">: {</span>
    <span class="text-blue-400">"name"</span><span class="text-slate-300">:</span> <span class="text-orange-400">"Jane Smith"</span><span class="text-slate-300">,</span>
    <span class="text-blue-400">"email"</span><span class="text-slate-300">:</span> <span class="text-orange-400">"jane@example.com"</span>
  <span class="text-slate-300">}</span>
<span class="text-purple-400">}</span></code></pre>
            </div>
            
            <!-- Right side: Explanation -->
            <div class="space-y-6">
              <h3 class="text-2xl font-semibold text-white">Intuitive API Design</h3>
              <p class="text-slate-300">
                HTTRPC follows RESTful principles while adding type safety through JSON Schema validation.
              </p>
              <ul class="space-y-4">
                <li class="flex items-start">
                  <div class="flex-shrink-0 h-6 w-6 rounded-full bg-cyan-500/20 flex items-center justify-center mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-cyan-400" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <span class="ml-3 text-slate-300">Consistent URL patterns for easy discovery</span>
                </li>
                <li class="flex items-start">
                  <div class="flex-shrink-0 h-6 w-6 rounded-full bg-cyan-500/20 flex items-center justify-center mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-cyan-400" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <span class="ml-3 text-slate-300">Standard HTTP methods and status codes</span>
                </li>
                <li class="flex items-start">
                  <div class="flex-shrink-0 h-6 w-6 rounded-full bg-cyan-500/20 flex items-center justify-center mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-cyan-400" viewBox="0 0 20 20" fill="currentColor">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd" />
                    </svg>
                  </div>
                  <span class="ml-3 text-slate-300">JSON Schema for request and response validation</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <!-- CTA Section -->
      <section id="getting-started" class="py-32 px-6 relative">
        <div class="max-w-4xl mx-auto text-center space-y-8">
          <h2 class="text-4xl md:text-5xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-cyan-400 to-blue-500">
            Ready to Simplify Your APIs?
          </h2>
          <p class="text-xl text-slate-300">
            Start building type-safe, language-agnostic APIs today with HTTRPC.
          </p>
          <div class="flex flex-wrap justify-center gap-6 pt-6">
            <a href="#" class="flex items-center px-6 py-3 bg-gradient-to-r from-blue-500 to-indigo-600 hover:from-blue-600 hover:to-indigo-700 text-white font-medium rounded-full transition-all duration-200">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9 4.804A7.968 7.968 0 005.5 4c-1.255 0-2.443.29-3.5.804v10A7.969 7.969 0 015.5 14c1.669 0 3.218.51 4.5 1.385A7.962 7.962 0 0114.5 14c1.255 0 2.443.29 3.5.804v-10A7.968 7.968 0 0014.5 4c-1.255 0-2.443.29-3.5.804V12a1 1 0 11-2 0V4.804z"/>
              </svg>
              <span>Read the Docs</span>
            </a>
            <a href="https://github.com/httrpc/httrpc/tree/main/examples" target="_blank" rel="noopener noreferrer" class="flex items-center px-6 py-3 bg-white/10 hover:bg-white/15 text-white font-medium rounded-full transition-all duration-200">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M12.316 3.051a1 1 0 01.633 1.265l-4 12a1 1 0 11-1.898-.632l4-12a1 1 0 011.265-.633zM5.707 6.293a1 1 0 010 1.414L3.414 10l2.293 2.293a1 1 0 11-1.414 1.414l-3-3a1 1 0 010-1.414l3-3a1 1 0 011.414 0zm8.586 0a1 1 0 011.414 0l3 3a1 1 0 010 1.414l-3 3a1 1 0 11-1.414-1.414L16.586 10l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd"/>
              </svg>
              <span>View Examples</span>
            </a>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="py-12 px-6 border-t border-white/10 bg-navy-900/30">
        <div class="max-w-7xl mx-auto">
          <div class="flex flex-col md:flex-row justify-between items-center">
            <div class="mb-6 md:mb-0">
              <div class="text-xl font-bold text-white">
                HTTRPC
              </div>
              <p class="text-slate-400 mt-2">A modern approach to API development</p>
            </div>
            <div class="flex flex-wrap gap-x-8 gap-y-4 justify-center">
              <a href="https://github.com/httrpc/httrpc" target="_blank" rel="noopener noreferrer" class="text-slate-300 hover:text-white transition-colors duration-200">GitHub</a>
              <a href="#" class="text-slate-300 hover:text-white transition-colors duration-200">Documentation</a>
              <a href="./SPEC.md" class="text-slate-300 hover:text-white transition-colors duration-200">Specification</a>
              <a href="#" class="text-slate-300 hover:text-white transition-colors duration-200">Examples</a>
            </div>
          </div>
          <div class="mt-8 pt-8 border-t border-white/10 text-center text-slate-400 text-sm">
            <p>HTTRPC Framework - Licensed under MIT</p>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<style>
/* Base styles */
:root {
  --navy-950: #0a0c1b;
  --navy-900: #0f1225;
}

body {
  @apply antialiased;
  background-color: var(--navy-950);
}

/* Background grid pattern */
.bg-grid-pattern {
  background-image: 
    linear-gradient(to right, rgba(255, 255, 255, 0.05) 1px, transparent 1px),
    linear-gradient(to bottom, rgba(255, 255, 255, 0.05) 1px, transparent 1px);
  background-size: 40px 40px;
}

/* Feature cards */
.feature-card {
  @apply p-6 rounded-xl bg-navy-900/50 border border-indigo-800/20 transition-all duration-300 hover:border-indigo-700/30;
}

.feature-icon {
  @apply w-12 h-12 rounded-xl flex items-center justify-center text-white;
}

/* Code container with subtle glow */
.code-container {
  position: relative;
}

.code-container::after {
  content: '';
  position: absolute;
  top: -20px;
  right: -20px;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.15) 0%, rgba(99, 102, 241, 0) 70%);
  z-index: -1;
}
</style>
