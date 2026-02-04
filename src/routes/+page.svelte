<script lang="ts">
  import { ArrowRight, CheckCircle2, Users, Zap, Target, TrendingUp, Clock, Shield, Award, Code2 } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "What makes this different from Salesforce or HubSpot?",
    "How long does implementation take?",
    "Can you integrate with our existing tools?",
    "What's included in the monthly support fee?",
    "Do you work with brokers outside the UK?",
    "Can we customise the pipeline stages?",
    "What happens if we need changes after launch?",
    "Is our data secure?"
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
            Stop fighting your CRM. Start closing deals.
          </h1>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#contact" class="inline-block bg-black text-white text-lg font-medium px-8 py-3.5 rounded-full hover:bg-gray-800 transition-colors">
              Book a call
            </a>
            <a href="#how-it-works" class="inline-block bg-white text-black border-2 border-gray-200 text-lg font-medium px-8 py-3.5 rounded-full hover:bg-gray-50 transition-colors">
              See how it works
            </a>
          </div>
        </div>

        <!-- Right: Description -->
        <div class="max-w-[500px] lg:mb-6">
          <p class="text-lg md:text-[1.15rem] leading-relaxed text-gray-800">
            Purpose-built pipeline management for brokers. Not another generic tool you have to bend your business around.
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
            <span class="font-medium text-gray-900">Pipeline CRM</span>
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
                <p class="font-medium text-gray-900 text-lg">Track deals from first contact through commission paid.</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Manage sub-broker networks with automatic commission splits and performance tracking.</p>
              </div>
            </div>

            <div class="flex gap-4 mb-6 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Send contracts for e-signature directly from deal records with automatic document attachment.</p>
              </div>
            </div>

            <div class="flex gap-4 opacity-40">
              <div class="w-4"></div> <!-- Spacer -->
              <div class="border-l-2 border-gray-300 pl-4 py-1">
                <p class="text-gray-800 text-lg leading-relaxed">Commission tracking that actually works — expected, pending, and received by deal and period.</p>
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
        <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full tracking-wide">LIVE DEMO</button>
        
        <!-- Language Selector -->
        <div class="flex items-center gap-1 pl-1 cursor-pointer">
          <img src="https://placehold.co/20x15/firebrick/white?text=US" alt="US Flag" class="w-5 h-auto rounded-sm">
          <svg xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-gray-500"><path d="m6 9 6 6 6-6"/></svg>
        </div>
      </div>

      <!-- Powered by text -->
      <div class="absolute bottom-4 right-1/2 translate-x-1/2 text-[10px] text-gray-500 opacity-50">
        Built for Brokers
      </div>

    </div>
  </section>

  <!-- Problem Section -->
  <section id="problem" class="max-w-[1200px] mx-auto px-6 py-24">
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-16 text-center">
      The problem
    </h2>
    
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <div class="bg-white rounded-2xl p-8 border border-gray-200">
        <h3 class="text-2xl font-semibold mb-4">Salesforce is overkill</h3>
        <p class="text-gray-600 leading-relaxed">
          Enterprise complexity you don't need. Six months to configure. Half your team still uses spreadsheets anyway.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 border border-gray-200">
        <h3 class="text-2xl font-semibold mb-4">HubSpot doesn't get brokers</h3>
        <p class="text-gray-600 leading-relaxed">
          Built for SaaS companies, not commission-based businesses. No sub-broker tracking. No supplier management. No deal attribution.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 border border-gray-200">
        <h3 class="text-2xl font-semibold mb-4">Spreadsheets are chaos</h3>
        <p class="text-gray-600 leading-relaxed">
          Multiple versions. No audit trail. Commission calculations held together with hope and nested IF statements.
        </p>
      </div>
    </div>

    <p class="text-center text-lg text-gray-600 max-w-3xl mx-auto mt-12">
      You're a broker, not a software administrator.
    </p>
  </section>

  <!-- Solution Section -->
  <section id="solution" class="max-w-[1400px] mx-auto px-6 py-24 relative">
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 text-center">
      The solution
    </h2>
    <p class="text-lg text-gray-600 max-w-3xl mx-auto mb-16 text-center">
      A CRM that speaks broker. Built by someone who's implemented CRM systems across energy, telecoms, and mortgage brokers. Every feature exists because a broker needed it.
    </p>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Feature 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-blue-600">01</span>
                </div>
                <h3 class="text-3xl font-medium">Deal pipeline that matches your reality</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                Custom stages for your actual sales process. From first contact through commission paid. Track what matters to your business, not what a generic CRM thinks you should track.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Custom pipeline stages</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Deal value tracking</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Commission forecasting</span>
                </li>
            </ul>
        </div>
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border border-blue-100 order-2 md:order-2 min-h-[400px] flex items-center justify-center">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6 mb-4">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
                            <Target size={20} class="text-blue-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Deal Pipeline</div>
                            <div class="text-xs text-gray-500">Active Deals</div>
                        </div>
                    </div>
                    <div class="space-y-2">
                        <div class="flex justify-between items-center p-2 bg-gray-50 rounded">
                            <span class="text-xs text-gray-600">First Contact</span>
                            <span class="text-xs font-bold">12</span>
                        </div>
                        <div class="flex justify-between items-center p-2 bg-blue-50 rounded border border-blue-200">
                            <span class="text-xs text-gray-900 font-medium">Proposal Sent</span>
                            <span class="text-xs font-bold text-blue-600">8</span>
                        </div>
                        <div class="flex justify-between items-center p-2 bg-gray-50 rounded">
                            <span class="text-xs text-gray-600">Contract Signed</span>
                            <span class="text-xs font-bold">5</span>
                        </div>
                        <div class="flex justify-between items-center p-2 bg-green-50 rounded">
                            <span class="text-xs text-gray-600">Commission Paid</span>
                            <span class="text-xs font-bold text-green-600">3</span>
                        </div>
                    </div>
                </div>
                <div class="grid grid-cols-3 gap-3">
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-gray-900">£48K</div>
                        <div class="text-[10px] text-gray-500">Pipeline Value</div>
                    </div>
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-gray-900">28</div>
                        <div class="text-[10px] text-gray-500">Active Deals</div>
                    </div>
                    <div class="bg-white rounded-lg p-3 text-center shadow-sm">
                        <div class="text-lg font-bold text-green-600">£12K</div>
                        <div class="text-[10px] text-gray-500">This Month</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Feature 2 Visual -->
        <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-2xl p-8 border border-purple-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center">
                            <Users size={20} class="text-purple-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Sub-Broker Network</div>
                            <div class="text-xs text-gray-500">Performance Overview</div>
                        </div>
                    </div>
                    <div class="space-y-3">
                        <div class="flex items-center justify-between p-3 bg-purple-50 rounded-lg border border-purple-200">
                            <div>
                                <div class="text-xs font-medium text-gray-900">Sarah Johnson</div>
                                <div class="text-[10px] text-gray-500">8 deals • £24K pipeline</div>
                            </div>
                            <div class="text-sm font-bold text-purple-600">£6,400</div>
                        </div>
                        <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                            <div>
                                <div class="text-xs font-medium text-gray-700">Mike Thompson</div>
                                <div class="text-[10px] text-gray-500">5 deals • £18K pipeline</div>
                            </div>
                            <div class="text-sm font-bold text-gray-900">£4,200</div>
                        </div>
                        <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg">
                            <div>
                                <div class="text-xs font-medium text-gray-700">Emma Davis</div>
                                <div class="text-[10px] text-gray-500">3 deals • £12K pipeline</div>
                            </div>
                            <div class="text-sm font-bold text-gray-900">£2,800</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-purple-600">02</span>
                </div>
                <h3 class="text-3xl font-medium">Sub-broker management built in</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                Track who brought in what. Calculate splits automatically. See performance at a glance. Your network is an asset — treat it like one.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Automatic commission splits</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Performance tracking</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Deal attribution</span>
                </li>
            </ul>
        </div>

        <!-- Feature 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-green-600">03</span>
                </div>
                <h3 class="text-3xl font-medium">E-signatures without the faff</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                Send contracts for signing directly from deal records. Track status. Auto-attach signed documents. One less tab to manage.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Send from deal records</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Real-time status tracking</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Automatic document attachment</span>
                </li>
            </ul>
        </div>
        <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-2xl p-8 border border-green-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center">
                            <CheckCircle2 size={20} class="text-green-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Contract Status</div>
                            <div class="text-xs text-gray-500">Active Documents</div>
                        </div>
                    </div>
                    <div class="space-y-3">
                        <div class="p-3 bg-green-50 rounded-lg border border-green-200">
                            <div class="flex justify-between items-center mb-1">
                                <div class="text-xs font-medium text-gray-900">Energy Supply Agreement</div>
                                <CheckCircle2 size={14} class="text-green-600" />
                            </div>
                            <div class="text-[10px] text-gray-500">Signed 2 hours ago</div>
                        </div>
                        <div class="p-3 bg-orange-50 rounded-lg border border-orange-200">
                            <div class="flex justify-between items-center mb-1">
                                <div class="text-xs font-medium text-gray-900">Telecoms Contract</div>
                                <Clock size={14} class="text-orange-600" />
                            </div>
                            <div class="text-[10px] text-gray-500">Awaiting signature</div>
                        </div>
                        <div class="p-3 bg-gray-50 rounded-lg border border-gray-200">
                            <div class="flex justify-between items-center mb-1">
                                <div class="text-xs font-medium text-gray-700">Broker Agreement</div>
                                <div class="text-[10px] text-gray-500">Draft</div>
                            </div>
                            <div class="text-[10px] text-gray-500">Ready to send</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Feature 4 -->
        <div class="flex flex-col justify-center order-7 md:order-7">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-orange-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-orange-600">04</span>
                </div>
                <h3 class="text-3xl font-medium">Commission tracking that actually works</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                Expected, pending, received. By deal, by sub-broker, by period. Forecasting you can trust because it's based on your real pipeline.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Expected vs actual tracking</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Period-based reporting</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Accurate forecasting</span>
                </li>
            </ul>
        </div>

        <div class="bg-gradient-to-br from-orange-50 to-amber-50 rounded-2xl p-8 border border-orange-100 min-h-[300px] flex items-center justify-center order-8 md:order-8">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-orange-100 rounded-lg flex items-center justify-center">
                            <TrendingUp size={20} class="text-orange-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Commission Overview</div>
                            <div class="text-xs text-gray-500">Q1 2024</div>
                        </div>
                    </div>
                    <div class="space-y-3">
                        <div class="p-3 bg-green-50 rounded-lg">
                            <div class="text-[10px] text-gray-500 mb-1">Received</div>
                            <div class="text-xl font-bold text-green-600">£42,800</div>
                        </div>
                        <div class="p-3 bg-orange-50 rounded-lg">
                            <div class="text-[10px] text-gray-500 mb-1">Pending</div>
                            <div class="text-xl font-bold text-orange-600">£28,400</div>
                        </div>
                        <div class="p-3 bg-blue-50 rounded-lg">
                            <div class="text-[10px] text-gray-500 mb-1">Expected (Pipeline)</div>
                            <div class="text-xl font-bold text-blue-600">£64,200</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Feature 5 -->
        <div class="bg-gradient-to-br from-indigo-50 to-purple-50 rounded-2xl p-8 border border-indigo-100 min-h-[300px] flex items-center justify-center order-10 md:order-9">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-indigo-100 rounded-lg flex items-center justify-center">
                            <Shield size={20} class="text-indigo-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Compliance Checklist</div>
                            <div class="text-xs text-gray-500">Deal #2847</div>
                        </div>
                    </div>
                    <div class="space-y-2">
                        <div class="flex items-center justify-between p-2 bg-green-50 rounded">
                            <span class="text-xs text-gray-700">ID Verification</span>
                            <CheckCircle2 size={14} class="text-green-600" />
                        </div>
                        <div class="flex items-center justify-between p-2 bg-green-50 rounded">
                            <span class="text-xs text-gray-700">Proof of Address</span>
                            <CheckCircle2 size={14} class="text-green-600" />
                        </div>
                        <div class="flex items-center justify-between p-2 bg-orange-50 rounded border border-orange-200">
                            <span class="text-xs text-gray-900 font-medium">Credit Check</span>
                            <Clock size={14} class="text-orange-600" />
                        </div>
                        <div class="flex items-center justify-between p-2 bg-gray-50 rounded opacity-50">
                            <span class="text-xs text-gray-500">Final Approval</span>
                            <div class="w-3 h-3 rounded-full border-2 border-gray-300"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="flex flex-col justify-center order-9 md:order-10">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-indigo-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-indigo-600">05</span>
                </div>
                <h3 class="text-3xl font-medium">Compliance without complexity</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                Document collection workflows. Audit trails. Approval chains. Stay regulated without drowning in admin.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Document collection workflows</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Complete audit trails</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Approval chain management</span>
                </li>
            </ul>
        </div>

        <!-- Feature 6 -->
        <div class="flex flex-col justify-center order-11 md:order-11">
            <div class="flex items-center gap-3 mb-4">
                <div class="w-10 h-10 bg-pink-100 rounded-lg flex items-center justify-center">
                    <span class="text-lg font-bold text-pink-600">06</span>
                </div>
                <h3 class="text-3xl font-medium">Reports that answer real questions</h3>
            </div>
            <p class="text-gray-600 leading-relaxed mb-6">
                "How much commission is pending from sub-broker X this quarter?" Get answers in seconds, not spreadsheet sessions.
            </p>
            <ul class="space-y-3">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Pre-built broker reports</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Custom report builder</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-gray-700">Real-time data updates</span>
                </li>
            </ul>
        </div>

        <div class="bg-gradient-to-br from-pink-50 to-rose-50 rounded-2xl p-8 border border-pink-100 min-h-[300px] flex items-center justify-center order-12 md:order-12">
            <div class="w-full max-w-md">
                <div class="bg-white rounded-xl shadow-lg p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-10 h-10 bg-pink-100 rounded-lg flex items-center justify-center">
                            <TrendingUp size={20} class="text-pink-600" />
                        </div>
                        <div>
                            <div class="text-sm font-semibold text-gray-900">Quick Reports</div>
                            <div class="text-xs text-gray-500">Most Used</div>
                        </div>
                    </div>
                    <div class="space-y-2">
                        <button class="w-full text-left p-3 bg-gray-50 rounded-lg hover:bg-gray-100 transition-colors">
                            <div class="text-xs font-medium text-gray-900">Commission by Sub-Broker</div>
                            <div class="text-[10px] text-gray-500">This quarter</div>
                        </button>
                        <button class="w-full text-left p-3 bg-gray-50 rounded-lg hover:bg-gray-100 transition-colors">
                            <div class="text-xs font-medium text-gray-900">Pipeline by Stage</div>
                            <div class="text-[10px] text-gray-500">Current month</div>
                        </button>
                        <button class="w-full text-left p-3 bg-gray-50 rounded-lg hover:bg-gray-100 transition-colors">
                            <div class="text-xs font-medium text-gray-900">Pending Commissions</div>
                            <div class="text-[10px] text-gray-500">All time</div>
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- Who It's For Section -->
  <section id="who-its-for" class="max-w-[1400px] mx-auto px-6 py-24 bg-gray-50 rounded-3xl">
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 text-center">
      Who it's for
    </h2>
    <p class="text-lg text-gray-600 max-w-3xl mx-auto mb-16 text-center">
      Built for brokers who earn on commission.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-white rounded-2xl p-8 border border-gray-200">
            <h3 class="text-2xl font-semibold mb-4">Energy brokers</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
                Manage supplier relationships, track contract renewals, and never miss a commission payment. Built with insight from the UK energy market.
            </p>
            <ul class="space-y-2">
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Supplier relationship management</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Contract renewal tracking</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Commission payment alerts</span>
                </li>
            </ul>
        </div>

        <div class="bg-white rounded-2xl p-8 border border-gray-200">
            <h3 class="text-2xl font-semibold mb-4">Telecoms brokers</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
                Complex deals, multiple carriers, ongoing commissions. Track it all in one place with attribution that actually makes sense.
            </p>
            <ul class="space-y-2">
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Multi-carrier deal management</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Recurring commission tracking</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Clear deal attribution</span>
                </li>
            </ul>
        </div>

        <div class="bg-white rounded-2xl p-8 border border-gray-200">
            <h3 class="text-2xl font-semibold mb-4">Mortgage brokers</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
                Application tracking, document management, compliance workflows. Purpose-built for regulated financial services.
            </p>
            <ul class="space-y-2">
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Application status tracking</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Document management system</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Compliance workflow automation</span>
                </li>
            </ul>
        </div>

        <div class="bg-white rounded-2xl p-8 border border-gray-200">
            <h3 class="text-2xl font-semibold mb-4">Insurance brokers</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
                Policy lifecycle management, renewal tracking, sub-agent networks. All the complexity, none of the spreadsheet chaos.
            </p>
            <ul class="space-y-2">
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Policy lifecycle tracking</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Renewal management</span>
                </li>
                <li class="flex items-start gap-2 text-sm text-gray-700">
                    <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span>Sub-agent network management</span>
                </li>
            </ul>
        </div>
    </div>
  </section>

  <!-- Pricing Section -->
  <section id="pricing" class="max-w-[1400px] mx-auto px-6 py-24">
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 text-center">
      Investment
    </h2>
    <p class="text-lg text-gray-600 max-w-3xl mx-auto mb-16 text-center">
      Transparent pricing. Real value. One-time build, then ongoing support to keep everything running smoothly.
    </p>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Starter -->
        <div class="bg-white rounded-2xl p-8 border-2 border-gray-200">
            <h3 class="text-2xl font-semibold mb-2">Pipeline Starter</h3>
            <div class="mb-6">
                <div class="text-4xl font-bold text-gray-900 mb-1">£6,000</div>
                <div class="text-sm text-gray-600">+ £400/month support</div>
            </div>
            <ul class="space-y-3 mb-8">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Single pipeline setup</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Contact & company management</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Basic commission tracking</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Standard reporting</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Email integration</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">2 user licences</span>
                </li>
            </ul>
            <a href="#contact" class="block w-full text-center bg-white text-black border-2 border-gray-200 px-6 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors">
                Get started
            </a>
        </div>

        <!-- Pro (Most Popular) -->
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border-2 border-blue-300 relative">
            <div class="absolute -top-4 left-1/2 -translate-x-1/2 bg-blue-600 text-white text-xs font-bold px-4 py-1.5 rounded-full">
                MOST POPULAR
            </div>
            <h3 class="text-2xl font-semibold mb-2">Pipeline Pro</h3>
            <div class="mb-6">
                <div class="text-4xl font-bold text-gray-900 mb-1">£12,000</div>
                <div class="text-sm text-gray-600">+ £750/month support</div>
            </div>
            <ul class="space-y-3 mb-8">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Everything in Starter</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Sub-broker management</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">E-signature integration</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Advanced commission splits</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Custom reporting dashboard</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Compliance workflows</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">10 user licences</span>
                </li>
            </ul>
            <a href="#contact" class="block w-full text-center bg-black text-white px-6 py-3 rounded-full font-medium hover:bg-gray-800 transition-colors">
                Get started
            </a>
        </div>

        <!-- Enterprise -->
        <div class="bg-white rounded-2xl p-8 border-2 border-gray-200">
            <h3 class="text-2xl font-semibold mb-2">Pipeline Enterprise</h3>
            <div class="mb-6">
                <div class="text-4xl font-bold text-gray-900 mb-1">£20,000+</div>
                <div class="text-sm text-gray-600">+ £1,200/month support</div>
            </div>
            <ul class="space-y-3 mb-8">
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Everything in Pro</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">AI-powered data queries</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Multi-team pipelines</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Supplier portal integrations</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">White-labelling options</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Custom automations</span>
                </li>
                <li class="flex items-start gap-3">
                    <CheckCircle2 size={18} class="text-green-600 mt-0.5 flex-shrink-0" />
                    <span class="text-sm text-gray-700">Unlimited users</span>
                </li>
            </ul>
            <a href="#contact" class="block w-full text-center bg-white text-black border-2 border-gray-200 px-6 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors">
                Get started
            </a>
        </div>
    </div>
  </section>

  <!-- How It Works Section -->
  <section id="how-it-works" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">How it works</h2>
        <p class="text-gray-600">Live in two weeks, not two quarters.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
        <!-- Step 1 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-blue-600">1</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Discovery call</h3>
            <p class="text-sm text-gray-600 leading-relaxed">
                30 minutes to understand your business. Your pipeline stages, commission structures, team size, pain points. No sales pitch — just questions.
            </p>
        </div>

        <!-- Step 2 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-purple-600">2</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Configuration & build</h3>
            <p class="text-sm text-gray-600 leading-relaxed">
                Your CRM built on a battle-tested foundation, customised to your exact workflow. You'll see progress throughout, not just at the end.
            </p>
        </div>

        <!-- Step 3 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-green-600">3</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Training & handover</h3>
            <p class="text-sm text-gray-600 leading-relaxed">
                Your team trained on the system. Documentation for everything. You're not dependent on me to use what I built.
            </p>
        </div>

        <!-- Step 4 -->
        <div class="bg-white rounded-3xl p-8 border border-gray-200 shadow-sm">
            <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center mb-4">
                <span class="text-xl font-bold text-orange-600">4</span>
            </div>
            <h3 class="text-xl font-semibold mb-3">Ongoing support</h3>
            <p class="text-sm text-gray-600 leading-relaxed">
                Issues handled within 24 hours. Monthly improvements included. Your CRM keeps getting better, not just maintained.
            </p>
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
                            This is built specifically for commission-based brokers. Salesforce is enterprise complexity you don't need. HubSpot is designed for SaaS companies. This has sub-broker tracking, commission splits, and supplier management built in — not bolted on.
                        {:else if i === 1}
                            Two weeks from discovery call to go-live. Week one is configuration and build. Week two is training and handover. You'll see progress throughout, not just at the end.
                        {:else if i === 2}
                            Yes. Email integration is standard. We can connect to most accounting software, e-signature platforms, and document storage systems. If you have specific integration needs, mention them in the discovery call.
                        {:else if i === 3}
                            Bug fixes within 24 hours. Monthly feature improvements based on your feedback. System updates and maintenance. Email and phone support during UK business hours.
                        {:else if i === 4}
                            Yes. While the system was built with insight from UK energy and telecoms brokers, it works for commission-based businesses anywhere. Pricing and support terms may vary by region.
                        {:else if i === 5}
                            Absolutely. Your pipeline stages are configured during the build phase to match your actual sales process. You can have as many stages as you need, named whatever makes sense for your business.
                        {:else if i === 6}
                            That's what the monthly support fee covers. Small changes and tweaks are included. Larger feature additions would be quoted separately, but you're never locked in — you own your data and can export it anytime.
                        {:else if i === 7}
                            Yes. Your data is encrypted at rest and in transit. Hosted on enterprise-grade infrastructure with daily backups. You can export your data at any time. We never sell or share your data with third parties.
                        {/if}
                    </div>
                {/if}
            </div>
          {/each}
      </div>
  </section>

  <!-- Bottom CTA -->
  <section id="contact" class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-4">Ready to stop fighting your tools?</h2>
      <p class="text-lg text-gray-600 mb-8 max-w-2xl">
        Book a 30-minute call. No pitch, no pressure. Just a conversation about whether this is right for your business.
      </p>
      <div class="flex flex-col sm:flex-row items-center gap-4">
          <a href="#contact" class="bg-black text-white px-8 py-4 rounded-full font-medium hover:bg-gray-800 transition-colors text-base">
              Book your call
          </a>
      </div>
      <p class="text-sm text-gray-500 mt-6">30-minute discovery call • No commitment required • See if it's a fit</p>
  </section>
</main>

