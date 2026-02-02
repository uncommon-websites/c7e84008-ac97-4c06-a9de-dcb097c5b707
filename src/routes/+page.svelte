<script lang="ts">
  import { ArrowRight, CheckCircle2, Users, Zap, Target, TrendingUp, Clock, Shield } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "What types of AI implementations do you specialize in?",
    "How long does a typical implementation take?",
    "Do you work with companies outside the mid-market?",
    "What is your pricing model?",
    "How do you measure ROI from AI implementations?",
    "Do you provide ongoing support after implementation?",
    "What industries do you serve?",
    "Can you integrate with our existing tech stack?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section (ALREADY CUSTOMIZED - DO NOT MODIFY) -->
  <section class="pt-16 md:pt-24 pb-0">
    <div class="max-w-[1600px] mx-auto px-6 md:px-10">
      
      <!-- Hero Text Content -->
      <div class="flex flex-col lg:flex-row lg:justify-between lg:items-end gap-10 mb-20">
        <!-- Left: Headline & CTA -->
        <div class="max-w-3xl">
          <h1 class="text-5xl md:text-[5.5rem] leading-[1.05] font-medium tracking-tight text-black mb-10">
            Strategic AI consultancy for business transformation
          </h1>
          <a href="#contact" class="inline-block bg-black text-white text-lg font-medium px-8 py-3.5 rounded-full hover:bg-gray-800 transition-colors">
            Book an AI strategy audit
          </a>
        </div>

        <!-- Right: Description -->
        <div class="max-w-[500px] lg:mb-6">
          <p class="text-lg md:text-[1.15rem] leading-relaxed text-gray-800">
            Built for operations leaders and scaling teams — eliminate bottlenecks with custom AI workflows and strategic automation pilots designed for rapid business transformation.
          </p>
        </div>
      </div>

    </div>

    <!-- Hero Visual / UI Mockup -->
    <div class="mx-4 md:mx-6 mt-8 rounded-t-[2.5rem] bg-gradient-to-br from-[#9baaf5] via-[#8e9bf0] to-[#9c78a8] pt-12 px-4 md:px-16 pb-0 overflow-hidden relative min-h-[600px]">
      
      <!-- The "Browser Window" / UI Container -->
      <div class="bg-white rounded-t-2xl shadow-2xl w-full h-full min-h-[800px] flex flex-col">
        
        <!-- UI Header -->
        <div class="flex items-center justify-between px-6 py-4 border-b border-gray-100">
          <div class="flex items-center gap-6">
            <span class="font-medium text-gray-900">Workflow AI</span>
            <div class="flex items-center gap-4 text-gray-400">
              <!-- Undo Icon -->
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 7v6h6"/><path d="M21 17a9 9 0 0 0-9-9 9 9 0 0 0-6 2.3L3 13"/></svg>
              <!-- Redo Icon -->
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 7v6h-6"/><path d="M3 17a9 9 0 0 1 9-9 9 9 0 0 1 6 2.3l3 3.7"/></svg>
            </div>
          </div>
          <div class="flex items-center gap-4">
            <span class="text-sm font-medium text-gray-500 cursor-pointer">Share</span>
            <button class="bg-black text-white text-sm font-medium px-4 py-1.5 rounded-md">Export</button>
          </div>
        </div>

        <!-- UI Body -->
        <div class="flex flex-col md:flex-row flex-1">
          
          <!-- Left Panel: Text Editor -->
          <div class="w-full md:w-1/2 p-8 md:p-12 border-r border-gray-100 relative">
            <!-- Sidebar Icons (simulated) -->
            <div class="absolute right-4 top-12 flex flex-col gap-6 text-gray-400">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="5"/><path d="M12 1v2"/><path d="M12 21v2"/><path d="M4.22 4.22l1.42 1.42"/><path d="M18.36 18.36l1.42 1.42"/><path d="M1 12h2"/><path d="M21 12h2"/><path d="M4.22 19.78l1.42-1.42"/><path d="M18.36 5.64l1.42-1.42"/></svg>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="3"/><path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1 0 2.83 2 2 0 0 1-2.83 0l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-2 2 2 2 0 0 1-2-2v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83 0 2 2 0 0 1 0-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1-2-2 2 2 0 0 1 2-2h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 0-2.83 2 2 0 0 1 2.83 0l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 2-2 2 2 0 0 1 2 2v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 0 2 2 0 0 1 0 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 2 2 2 2 0 0 1-2 2h-.09a1.65 1.65 0 0 0-1.51 1z"/></svg>
            </div>

            <div class="flex gap-4 mb-6">
              <!-- Blue Dot Indicator -->
              <div class="mt-1.5">
                <div class="w-4 h-4 rounded-full bg-gradient-to-br from-blue-400 to-blue-600 shadow-sm"></div>
              </div>
              <!-- Active Line -->
              <div class="border-l-2 border-gray-800 pl-4 py-1">
                <p class="font-medium text-gray-900 text-lg">Flowgrid automates your core business operations.</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Bridge the gap between strategy and execution with custom AI integrations tailored for your team's specific stack.</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Overcome implementation fears with rapid workflow automation pilots and proven frameworks designed for mid-market leaders.</p>
              </div>
            </div>

            <div class="flex gap-4 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Our implementation roadmap ensures measurable ROI within weeks of deployment.</p>
              </div>
            </div>
          </div>

          <!-- Right Panel: Image -->
          <div class="w-full md:w-1/2 p-8 flex items-center justify-center bg-gray-50">
            <div class="w-full h-full max-h-[500px] rounded-lg overflow-hidden shadow-lg relative">
              <!-- AI Consultant working -->
              <img src="/generated/image-professional-business-consultant-working-1770069847072-0.webp" alt="AI Strategy Consultant" class="w-full h-full object-cover">
              <!-- Overlay gradient -->
              <div class="absolute inset-0 bg-gradient-to-t from-orange-500/40 to-transparent mix-blend-overlay"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Floating Voice Chat Widget -->
      <div class="absolute bottom-8 right-8 md:bottom-12 md:right-12 bg-white rounded-full p-1.5 pr-4 shadow-[0_8px_30px_rgb(0,0,0,0.12)] flex items-center gap-3 z-20">
        <!-- Orb Icon -->
        <img src="https://placehold.co/40x40/3b82f6/white?text=AI" alt="AI Orb" class="w-10 h-10 rounded-full">
        
        <!-- Button -->
        <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full tracking-wide">AI PILOT</button>
        
        <!-- Language Selector -->
        <div class="flex items-center gap-1 pl-1 cursor-pointer">
          <img src="https://placehold.co/20x15/firebrick/white?text=US" alt="US Flag" class="w-5 h-auto rounded-sm">
          <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-500"><path d="m6 9 6 6 6-6"/></svg>
        </div>
      </div>

      <!-- Powered by text -->
      <div class="absolute bottom-4 right-1/2 translate-x-1/2 text-[10px] text-gray-500 opacity-50">
        Powered by Flowgrid Strategy
      </div>

    </div>
  </section>

  <!-- Services Overview Section -->
  <section id="services" class="max-w-[1200px] mx-auto px-6 py-24 text-center">
    <span class="text-sm font-medium text-gray-500 mb-4 block uppercase tracking-wider">Our Services</span>
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 leading-tight">
      Full-spectrum AI implementation — from strategic planning to market-ready products
    </h2>
    
    <div class="flex flex-wrap justify-center gap-x-6 gap-y-3 text-sm text-gray-700 mb-10">
      <span class="flex items-center gap-2 px-4 py-2 bg-gray-50 rounded-full border border-gray-100 font-medium">
        <Zap size={16} class="text-blue-600" /> Workflow Integration
      </span>
      <span class="flex items-center gap-2 px-4 py-2 bg-gray-50 rounded-full border border-gray-100 font-medium">
        <Target size={16} class="text-purple-600" /> Internal Tool Development
      </span>
      <span class="flex items-center gap-2 px-4 py-2 bg-gray-50 rounded-full border border-gray-100 font-medium">
        <TrendingUp size={16} class="text-green-600" /> GTM Product Strategy
      </span>
      <span class="flex items-center gap-2 px-4 py-2 bg-gray-50 rounded-full border border-gray-100 font-medium">
        <Clock size={16} class="text-orange-600" /> Rapid Pilots
      </span>
      <span class="flex items-center gap-2 px-4 py-2 bg-gray-50 rounded-full border border-gray-100 font-medium">
        <Shield size={16} class="text-indigo-600" /> Strategic Planning
      </span>
    </div>

    <p class="text-lg text-gray-600 max-w-3xl mx-auto mb-8">
      We bridge the gap between AI potential and business reality. Our proven frameworks help mid-market operations leaders implement AI solutions that deliver measurable ROI within weeks, not months.
    </p>
  </section>

  <!-- Core Services Section -->
  <section id="core-services" class="max-w-[1400px] mx-auto px-6 py-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Service 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <h3 class="text-3xl font-medium mb-4">AI Workflow Integration</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Transform your existing business processes with strategic AI automation. We analyze your current workflows, identify bottlenecks, and implement custom AI solutions that integrate seamlessly with your existing tech stack — delivering immediate efficiency gains.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Process automation and optimization</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Custom AI model integration</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Seamless tech stack compatibility</span>
                </li>
            </ul>
        </div>
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border border-blue-100 order-2 md:order-2 min-h-[400px] flex items-center justify-center">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6 mb-4">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
                            <Zap size={20} class="text-blue-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Workflow Automation</div>
                            <div class="text-xs text-gray-500">Active Process</div>
                        </div>
                    </div>
                    <div class="space-y-2">
                        <div class="h-2 bg-blue-100 rounded-full overflow-hidden">
                            <div class="h-full bg-blue-600 rounded-full" style="width: 85%"></div>
                        </div>
                        <div class="text-xs text-gray-600">85% efficiency improvement</div>
                    </div>
                </div>
                <div class="grid grid-cols-3 gap-3">
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-gray-900">-60%</div>
                        <div class="text-[10px] text-gray-500">Processing Time</div>
                    </div>
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-gray-900">+40%</div>
                        <div class="text-[10px] text-gray-500">Throughput</div>
                    </div>
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-gray-900">98%</div>
                        <div class="text-[10px] text-gray-500">Accuracy</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Service 2 -->
        <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-2xl p-8 border border-purple-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center">
                            <Target size={20} class="text-purple-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Internal Tool</div>
                            <div class="text-xs text-gray-500">Development Pipeline</div>
                        </div>
                    </div>
                    <div class="space-y-3">
                        <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                            <span class="text-xs font-medium text-gray-700">Discovery</span>
                            <CheckCircle2 size={16} class="text-green-600" />
                        </div>
                        <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                            <span class="text-xs font-medium text-gray-700">Prototype</span>
                            <CheckCircle2 size={16} class="text-green-600" />
                        </div>
                        <div class="flex items-center justify-between p-3 bg-purple-100 rounded-lg border-2 border-purple-300">
                            <span class="text-xs font-medium text-gray-900">Build & Deploy</span>
                            <div class="w-4 h-4 rounded-full bg-purple-600 animate-pulse"></div>
                        </div>
                        <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg opacity-50">
                            <span class="text-xs font-medium text-gray-700">Scale & Optimize</span>
                            <div class="w-4 h-4 rounded-full border-2 border-gray-300"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <h3 class="text-3xl font-medium mb-4">Internal Tool Development</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Build custom AI-powered tools that solve your team's unique operational challenges. From data processing automation to intelligent dashboards, we develop internal tools that enhance productivity and decision-making across your organization.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Custom dashboard development</span>
                </li>
                <li class="flex itemms-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Data processing automation</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Team-specific AI assistants</span>
                </li>
            </ul>
        </div>

        <!-- Service 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <h3 class="text-3xl font-medium mb-4">GTM Product Development</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Transform your AI innovation into market-ready products. We guide you through the entire go-to-market journey — from product strategy and development to launch planning and market positioning — ensuring your AI solution resonates with your target customers.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Product strategy & positioning</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">MVP development & testing</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Launch planning & execution</span>
                </li>
            </ul>
        </div>
        <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-2xl p-8 border border-green-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center">
                            <TrendingUp size={20} class="text-green-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Product Roadmap</div>
                            <div class="text-xs text-gray-500">Q1 2024 Launch</div>
                        </div>
                    </div>
                    <div class="space-y-3">
                        <div class="p-3 bg-green-50 rounded-lg border border-green-200">
                            <div class="text-xs font-medium text-gray-900 mb-1">Phase 1: Market Research</div>
                            <div class="h-1.5 bg-green-200 rounded-full overflow-hidden">
                                <div class="h-full bg-green-600 rounded-full" style="width: 100%"></div>
                            </div>
                        </div>
                        <div class="p-3 bg-green-50 rounded-lg border border-green-200">
                            <div class="text-xs font-medium text-gray-900 mb-1">Phase 2: MVP Development</div>
                            <div class="h-1.5 bg-green-200 rounded-full overflow-hidden">
                                <div class="h-full bg-green-600 rounded-full" style="width: 75%"></div>
                            </div>
                        </div>
                        <div class="p-3 bg-gray-50 rounded-lg border border-gray-200">
                            <div class="text-xs font-medium text-gray-700 mb-1">Phase 3: Beta Testing</div>
                            <div class="h-1.5 bg-gray-200 rounded-full overflow-hidden">
                                <div class="h-full bg-gray-400 rounded-full" style="width: 30%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- Process Section -->
  <section id="process" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Our proven implementation process</h2>
        <p class="text-gray-600">From initial discovery to full deployment, we follow a structured approach that ensures rapid results and measurable ROI at every stage.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
        <!-- Step 1 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-blue-600">1</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Discovery & Audit</h3>
            <p class="text-sm text-gray-600 leading-relaxed mb-4">
                We analyze your current workflows, identify bottlenecks, and map opportunities for AI integration.
            </p>
            <div class="text-xs text-gray-500 font-medium">Timeline: 1-2 weeks</div>
        </div>

        <!-- Step 2 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-purple-600">2</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Strategy & Planning</h3>
            <p class="text-sm text-gray-600 leading-relaxed mb-4">
                Develop a comprehensive implementation roadmap with clear milestones and ROI projections.
            </p>
            <div class="text-xs text-gray-500 font-medium">Timeline: 1 week</div>
        </div>

        <!-- Step 3 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-green-600">3</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Rapid Pilot</h3>
            <p class="text-sm text-gray-600 leading-relaxed mb-4">
                Launch a focused automation pilot to demonstrate value and gather real-world performance data.
            </p>
            <div class="text-xs text-gray-500 font-medium">Timeline: 2-4 weeks</div>
        </div>

        <!-- Step 4 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-orange-600">4</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Scale & Optimize</h3>
            <p class="text-sm text-gray-600 leading-relaxed mb-4">
                Expand successful implementations across your organization with ongoing optimization and support.
            </p>
            <div class="text-xs text-gray-500 font-medium">Timeline: Ongoing</div>
        </div>
    </div>
  </section>

  <!-- Results & Testimonials -->
  <section id="results" class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Trusted by scaling operations teams</h2>
        <p class="text-gray-600">See how mid-market leaders are transforming their businesses with strategic AI implementation.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
        <!-- Result 1 -->
        <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
            <div class="text-4xl font-bold text-gray-900 mb-2">60%</div>
            <div class="text-sm font-medium text-gray-700 mb-3">Faster Processing Time</div>
            <p class="text-xs text-gray-500 leading-relaxed">Operations team reduced manual data processing from 8 hours to 3 hours daily with custom AI workflow.</p>
        </div>

        <!-- Result 2 -->
        <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
            <div class="text-4xl font-bold text-gray-900 mb-2">$2.4M</div>
            <div class="text-sm font-medium text-gray-700 mb-3">Annual Cost Savings</div>
            <p class="text-xs text-gray-500 leading-relaxed">Mid-market SaaS company eliminated need for 6 FTE positions through intelligent automation.</p>
        </div>

        <!-- Result 3 -->
        <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
            <div class="text-4xl font-bold text-gray-900 mb-2">3 weeks</div>
            <div class="text-sm font-medium text-gray-700 mb-3">To First ROI</div>
            <p class="text-xs text-gray-500 leading-relaxed">E-commerce operations team saw measurable efficiency gains within first month of pilot deployment.</p>
        </div>
    </div>

    <!-- Testimonials -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border border-blue-100">
            <div class="flex items-start gap-4 mb-4">
                <img src="/generated/image-confident-male-executive-in-business-cas-1770069849604-1.webp" alt="Michael Chen" class="w-14 h-14 rounded-full object-cover" />
                <div>
                    <div class="font-semibold text-gray-900">Michael Chen</div>
                    <div class="text-sm text-gray-600">VP Operations, TechScale Inc.</div>
                </div>
            </div>
            <p class="text-gray-700 leading-relaxed italic">
                "Flowgrid transformed our operations in weeks, not months. Their rapid pilot approach let us see real results before committing to a full rollout. We're now processing 3x more customer requests with the same team size."
            </p>
        </div>

        <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-2xl p-8 border border-purple-100">
            <div class="flex items-start gap-4 mb-4">
                <img src="/generated/image-professional-female-business-leader-in-h-1770069851754-2.webp" alt="Sarah Martinez" class="w-14 h-14 rounded-full object-cover" />
                <div>
                    <div class="font-semibold text-gray-900">Sarah Martinez</div>
                    <div class="text-sm text-gray-600">COO, GrowthCo</div>
                </div>
            </div>
            <p class="text-gray-700 leading-relaxed italic">
                "Finally, an AI consultancy that understands mid-market constraints. No enterprise-level budgets required, no six-month timelines. Just practical solutions that work with our existing stack."
            </p>
        </div>
    </div>
  </section>

  <!-- Why Choose Us Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gray-50 rounded-3xl">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Why mid-market leaders choose Flowgrid</h2>
        <p class="text-gray-600">We understand the unique challenges of scaling businesses — limited resources, tight timelines, and the need for proven results.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-4">
                <Clock size={24} class="text-blue-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Rapid Implementation</h3>
            <p class="text-sm text-gray-600 leading-relaxed">See results in weeks, not months. Our rapid pilot approach delivers measurable value quickly.</p>
        </div>

        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-4">
                <Target size={24} class="text-purple-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Mid-Market Focus</h3>
            <p class="text-sm text-gray-600 leading-relaxed">Solutions designed for your scale — no enterprise budgets or resources required.</p>
        </div>

        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mb-4">
                <CheckCircle2 size={24} class="text-green-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Proven Frameworks</h3>
            <p class="text-sm text-gray-600 leading-relaxed">Battle-tested methodologies that eliminate implementation fears and reduce risk.</p>
        </div>

        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-orange-100 rounded-lg flex items-center justify-center mb-4">
                <Zap size={24} class="text-orange-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Stack Integration</h3>
            <p class="text-sm text-gray-600 leading-relaxed">Work with your existing tools and systems — no expensive platform migrations.</p>
        </div>

        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-indigo-100 rounded-lg flex items-center justify-center mb-4">
                <Users size={24} class="text-indigo-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Hands-On Support</h3>
            <p class="text-sm text-gray-600 leading-relaxed">Direct access to our team throughout implementation and beyond.</p>
        </div>

        <div class="bg-white rounded-xl p-6 shadow-sm">
            <div class="w-12 h-12 bg-pink-100 rounded-lg flex items-center justify-center mb-4">
                <TrendingUp size={24} class="text-pink-600" />
            </div>
            <h3 class="text-lg font-semibold mb-2">Measurable ROI</h3>
            <p class="text-sm text-gray-600 leading-relaxed">Clear metrics and KPIs tracked from day one to demonstrate business impact.</p>
        </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24">
      <h2 class="text-3xl font-medium mb-12">Frequently asked questions</h2>
      
      <div class="divide-y divide-gray-100">
          {#each faqs as question, i}
            <div class="py-4">
                <button class="w-full flex items-center justify-between text-left group" on:click={() => toggleFaq(i)}>
                    <span class="text-sm md:text-base text-gray-700 group-hover:text-black transition-colors font-medium">{question}</span>
                    <span class="text-gray-400">
                        <ArrowRight size={16} class="transition-transform duration-200 {openFaq === i ? 'rotate-90' : ''}" />
                    </span>
                </button>
                {#if openFaq === i}
                    <div class="mt-4 text-sm text-gray-600 leading-relaxed pb-2">
                        {#if i === 0}
                            We specialize in workflow automation, internal tool development, and go-to-market product strategy. Our focus is on practical AI implementations that integrate with your existing tech stack and deliver measurable ROI.
                        {:else if i === 1}
                            Our rapid pilot approach typically delivers initial results within 2-4 weeks. Full implementation timelines vary based on scope, but most projects reach production deployment within 6-8 weeks.
                        {:else if i === 2}
                            While we specialize in mid-market companies (50-500 employees), we work with any scaling business that needs rapid AI implementation without enterprise-level budgets or timelines.
                        {:else if i === 3}
                            We offer project-based pricing and retainer options. Pricing depends on scope and complexity, but we're designed to be accessible to mid-market budgets. Contact us for a custom quote.
                        {:else if i === 4}
                            We establish clear KPIs before implementation and track metrics like processing time reduction, cost savings, throughput improvements, and error rate decreases. Most clients see measurable ROI within 3-4 weeks.
                        {:else if i === 5}
                            Yes. We provide ongoing optimization, monitoring, and support packages to ensure your AI solutions continue delivering value as your business scales.
                        {:else if i === 6}
                            We work across industries including technology, financial services, healthcare, e-commerce, SaaS, and professional services. Our frameworks adapt to industry-specific requirements.
                        {:else if i === 7}
                            Absolutely. Stack integration is a core part of our approach. We work with your existing tools and platforms — no expensive migrations or platform changes required.
                        {/if}
                    </div>
                {/if}
            </div>
          {/each}
      </div>
  </section>

  <!-- Bottom CTA -->
  <section id="contact" class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-4">Ready to transform your operations with AI?</h2>
      <p class="text-lg text-gray-600 mb-8 max-w-2xl">
        Book a free AI strategy audit and discover how we can help you implement automation that delivers measurable ROI in weeks.
      </p>
      <div class="flex flex-col sm:flex-row items-center gap-4">
          <a href="#audit" class="bg-black text-white px-8 py-4 rounded-full font-medium hover:bg-gray-800 transition-colors text-base">
              Book your free audit
          </a>
          <a href="#contact" class="bg-white text-black border-2 border-gray-200 px-8 py-4 rounded-full font-medium hover:bg-gray-50 transition-colors text-base">
              Talk to our team
          </a>
      </div>
      <p class="text-sm text-gray-500 mt-6">No commitment required • 30-minute consultation • Custom implementation roadmap</p>
  </section>
</main>

