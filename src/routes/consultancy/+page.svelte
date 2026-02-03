<script lang="ts">
  import { ArrowRight, CheckCircle2, Users, Zap, Target, TrendingUp, Clock, Shield, Briefcase, LineChart, Award, MessageSquare, FileText, Calendar } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "What makes your consultancy approach different?",
    "How do you ensure ROI from AI investments?",
    "What size companies do you typically work with?",
    "Do you provide training for our team?",
    "How do you handle data security and privacy?",
    "What's included in the initial consultation?",
    "Can you work with our existing vendors?",
    "What happens after the initial implementation?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }

  // Engagement models
  const engagementModels = [
    {
      title: "Strategic Advisory",
      duration: "3-6 months",
      ideal: "Leadership teams planning AI transformation",
      deliverables: ["AI readiness assessment", "Strategic roadmap", "Technology recommendations", "Change management plan"]
    },
    {
      title: "Implementation Partnership",
      duration: "6-12 months",
      ideal: "Operations teams executing AI projects",
      deliverables: ["Full-stack implementation", "Custom tool development", "Team training", "Ongoing optimization"]
    },
    {
      title: "Rapid Pilot Program",
      duration: "4-8 weeks",
      ideal: "Teams testing AI viability",
      deliverables: ["Focused use case", "Proof of concept", "ROI analysis", "Scale-up recommendations"]
    },
    {
      title: "AI Training - Anthropic Focused",
      duration: "2-4 weeks",
      ideal: "Teams building expertise with Claude and Anthropic AI",
      deliverables: ["Hands-on Claude workshops", "Prompt engineering mastery", "Best practices guide", "Custom use case development"]
    }
  ];

  // Industry expertise
  const industries = [
    { name: "Financial Services", icon: Briefcase, color: "blue", focus: "Risk analysis, fraud detection, customer insights" },
    { name: "Healthcare", icon: Shield, color: "green", focus: "Patient data analysis, operational efficiency, diagnostics support" },
    { name: "Technology & SaaS", icon: Zap, color: "purple", focus: "Product intelligence, customer success automation, development acceleration" },
    { name: "E-commerce & Retail", icon: TrendingUp, color: "orange", focus: "Demand forecasting, personalization, supply chain optimization" },
    { name: "Professional Services", icon: FileText, color: "indigo", focus: "Knowledge management, client insights, proposal automation" },
    { name: "Manufacturing", icon: Target, color: "red", focus: "Quality control, predictive maintenance, supply chain intelligence" }
  ];
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section -->
  <section class="pt-16 md:pt-24 pb-12">
    <div class="max-w-[1400px] mx-auto px-6 md:px-10">
      
      <!-- Breadcrumb -->
      <div class="flex items-center gap-2 text-sm text-gray-500 mb-8">
        <a href="/" class="hover:text-gray-900 transition-colors">Home</a>
        <ArrowRight size={14} />
        <span class="text-gray-900 font-medium">Consultancy</span>
      </div>

      <!-- Hero Content -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center mb-16">
        <div>
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-blue-50 rounded-full text-sm font-medium text-blue-700 mb-6">
            <Briefcase size={16} />
            Strategic AI Consultancy
          </div>
          <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black mb-6 leading-[1.1]">
            Transform your business with expert AI guidance
          </h1>
          <p class="text-xl text-gray-600 leading-relaxed mb-8">
            Partner with experienced AI consultants who understand both the technology and your business challenges. We deliver strategic insights and hands-on implementation that drives measurable results.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#contact" class="inline-flex items-center justify-center gap-2 bg-black text-white text-base font-medium px-8 py-4 rounded-full hover:bg-gray-800 transition-colors">
              Schedule consultation
              <ArrowRight size={18} />
            </a>
            <a href="#approach" class="inline-flex items-center justify-center gap-2 bg-white text-black border-2 border-gray-200 text-base font-medium px-8 py-4 rounded-full hover:bg-gray-50 transition-colors">
              Our approach
            </a>
          </div>
        </div>

        <!-- Hero Image -->
        <div class="relative">
          <div class="aspect-[4/3] rounded-3xl overflow-hidden shadow-2xl">
            <img src="/generated/image-professional-business-consultant-working-1770069847072-0.webp" alt="AI Consultancy Team" class="w-full h-full object-cover" />
          </div>
          <!-- Floating Stats Card -->
          <div class="absolute -bottom-6 -left-6 bg-white rounded-2xl shadow-xl p-6 border border-gray-100">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center">
                <Award size={24} class="text-green-600" />
              </div>
              <div>
                <div class="text-2xl font-bold text-gray-900">50+</div>
                <div class="text-sm text-gray-600">Successful implementations</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Trust Indicators -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 pt-12 border-t border-gray-100">
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">3 months</div>
          <div class="text-sm text-gray-600">Average time to ROI</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">$2.4M</div>
          <div class="text-sm text-gray-600">Average annual savings</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">98%</div>
          <div class="text-sm text-gray-600">Client satisfaction rate</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">6+</div>
          <div class="text-sm text-gray-600">Industries served</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services Modules Section -->
  <section id="services" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-20">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Our service modules</h2>
      <p class="text-xl text-gray-600">
        Choose the right engagement model for your business transformation journey. Each module is designed to deliver measurable results and strategic value.
      </p>
    </div>

    <!-- 4 Key Service Modules -->
    <div class="space-y-24">
      
      <!-- Module 1: Strategic Advisory -->
      <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-3xl p-12 border border-blue-100">
        <div class="flex items-start justify-between mb-8">
          <div class="flex items-start gap-6">
            <div class="w-16 h-16 bg-blue-600 rounded-2xl flex items-center justify-center flex-shrink-0">
              <Target size={32} class="text-white" />
            </div>
            <div>
              <h3 class="text-3xl font-semibold mb-3">Strategic Advisory</h3>
              <p class="text-lg text-gray-700">Leadership teams planning AI transformation</p>
            </div>
          </div>
          <div class="text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-blue-600 text-white rounded-full text-sm font-medium mb-2">
              <Clock size={16} />
              3-6 months
            </div>
            <div class="text-sm text-gray-600">Engagement duration</div>
          </div>
        </div>

        <!-- What You Get -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">What you get</h4>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Comprehensive AI readiness assessment</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Strategic AI roadmap with clear milestones</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Technology stack recommendations</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Change management and adoption plan</span>
            </div>
          </div>
        </div>

        <!-- How You Get It -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">How you get it</h4>
          <p class="text-gray-700 leading-relaxed">
            We begin with stakeholder interviews and business analysis to understand your current state. Our team conducts a comprehensive technology audit and market analysis. You'll receive weekly strategy sessions with our senior consultants, culminating in a detailed presentation of your custom AI transformation roadmap with executive buy-in materials.
          </p>
        </div>

        <!-- Why It's Important -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">Why it's important to your business</h4>
          <p class="text-gray-700 leading-relaxed">
            Without a clear AI strategy, companies waste millions on disconnected initiatives that fail to deliver ROI. Our strategic advisory ensures your AI investments align with business objectives, avoiding costly mistakes and accelerating time-to-value. Leadership teams gain the confidence and roadmap needed to drive successful transformation across the organization.
          </p>
        </div>

        <!-- Example -->
        <div class="bg-white rounded-2xl p-8 border border-blue-200">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">Real-world example</h4>
          <div class="mb-4">
            <p class="text-gray-700 leading-relaxed mb-4">
              <span class="font-semibold text-gray-900">Client:</span> $50M SaaS company planning enterprise AI transformation with limited internal expertise.
            </p>
            <p class="text-gray-700 leading-relaxed mb-4">
              <span class="font-semibold text-gray-900">Challenge:</span> Leadership team lacked clarity on where to start, which technologies to invest in, and how to measure success.
            </p>
          </div>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 pt-4 border-t border-blue-100">
            <div>
              <h5 class="font-semibold text-gray-900 mb-3 flex items-center gap-2">
                <TrendingUp size={20} class="text-green-600" />
                Value delivered
              </h5>
              <ul class="space-y-2 text-sm text-gray-700">
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                  <span>Comprehensive AI readiness assessment completed in 4 weeks</span>
                </li>
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                  <span>18-month strategic roadmap with prioritized initiatives</span>
                </li>
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                  <span>Technology stack recommendations with vendor analysis</span>
                </li>
              </ul>
            </div>
            <div>
              <h5 class="font-semibold text-gray-900 mb-3 flex items-center gap-2">
                <Award size={20} class="text-blue-600" />
                Business outcome
              </h5>
              <ul class="space-y-2 text-sm text-gray-700">
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
                  <span><strong>$3.2M budget</strong> allocated with board approval</span>
                </li>
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
                  <span><strong>Avoided $800K</strong> in misaligned technology investments</span>
                </li>
                <li class="flex items-start gap-2">
                  <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
                  <span><strong>Clear ROI projections</strong> for each initiative phase</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Module 2: Implementation Partnership -->
      <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-3xl p-12 border border-purple-100">
        <div class="flex items-start justify-between mb-8">
          <div class="flex items-start gap-6">
            <div class="w-16 h-16 bg-purple-600 rounded-2xl flex items-center justify-center flex-shrink-0">
              <Zap size={32} class="text-white" />
            </div>
            <div>
              <h3 class="text-3xl font-semibold mb-3">Implementation Partnership</h3>
              <p class="text-lg text-gray-700">Operations teams executing AI projects</p>
            </div>
          </div>
          <div class="text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-purple-600 text-white rounded-full text-sm font-medium mb-2">
              <Clock size={16} />
              6-12 months
            </div>
            <div class="text-sm text-gray-600">Engagement duration</div>
          </div>
        </div>

        <!-- What You Get -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">What you get</h4>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-purple-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Full-stack AI implementation</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-purple-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Custom tool development and integration</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-purple-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Comprehensive team training programs</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-purple-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Ongoing optimization and support</span>
            </div>
          </div>
        </div>

        <!-- How You Get It -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">How you get it</h4>
          <p class="text-gray-700 leading-relaxed">
            Our embedded team works alongside your operations staff through agile sprints. We follow a phased approach starting with infrastructure setup, moving through development and testing cycles, and ending with full deployment. You'll have daily standups, bi-weekly sprint reviews, and continuous access to our technical team for seamless integration with your existing workflows.
          </p>
        </div>

        <!-- Why It's Important -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">Why it's important to your business</h4>
          <p class="text-gray-700 leading-relaxed">
            Successful AI implementation requires deep integration with existing systems and processes. Our partnership approach ensures solutions actually work in your environment, not just in theory. Operations teams gain efficiency improvements that compound over time, while building internal AI capabilities that reduce long-term dependency on external consultants.
          </p>
        </div>
      </div>

      <!-- Module 3: Rapid Pilot Program -->
      <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-3xl p-12 border border-green-100">
        <div class="flex items-start justify-between mb-8">
          <div class="flex items-start gap-6">
            <div class="w-16 h-16 bg-green-600 rounded-2xl flex items-center justify-center flex-shrink-0">
              <TrendingUp size={32} class="text-white" />
            </div>
            <div>
              <h3 class="text-3xl font-semibold mb-3">Rapid Pilot Program</h3>
              <p class="text-lg text-gray-700">Teams testing AI viability</p>
            </div>
          </div>
          <div class="text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-green-600 text-white rounded-full text-sm font-medium mb-2">
              <Clock size={16} />
              4-8 weeks
            </div>
            <div class="text-sm text-gray-600">Engagement duration</div>
          </div>
        </div>

        <!-- What You Get -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">What you get</h4>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Focused use case implementation</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Working proof of concept</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Detailed ROI analysis and projections</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-green-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Scale-up recommendations and roadmap</span>
            </div>
          </div>
        </div>

        <!-- How You Get It -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">How you get it</h4>
          <p class="text-gray-700 leading-relaxed">
            We kick off with a rapid discovery workshop to identify your highest-impact use case. Our team builds a working prototype in the first two weeks, then refines it based on your feedback. You'll see tangible results quickly with weekly demos, real-time performance tracking, and a final presentation showing clear ROI metrics and next-step recommendations.
          </p>
        </div>

        <!-- Why It's Important -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">Why it's important to your business</h4>
          <p class="text-gray-700 leading-relaxed">
            Testing AI viability before full commitment saves time and budget while reducing risk. Our rapid pilots prove value quickly, giving stakeholders confidence to invest in larger initiatives. Teams see real results in weeks, not months, enabling faster decision-making and competitive advantage in your market.
          </p>
        </div>
      </div>

      <!-- Module 4: AI Training - Anthropic Focused -->
      <div class="bg-gradient-to-br from-orange-50 to-amber-50 rounded-3xl p-12 border border-orange-100">
        <div class="flex items-start justify-between mb-8">
          <div class="flex items-start gap-6">
            <div class="w-16 h-16 bg-orange-600 rounded-2xl flex items-center justify-center flex-shrink-0">
              <Users size={32} class="text-white" />
            </div>
            <div>
              <h3 class="text-3xl font-semibold mb-3">AI Training - Anthropic Focused</h3>
              <p class="text-lg text-gray-700">Teams building expertise with Claude and Anthropic AI</p>
            </div>
          </div>
          <div class="text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-orange-600 text-white rounded-full text-sm font-medium mb-2">
              <Clock size={16} />
              2-4 weeks
            </div>
            <div class="text-sm text-gray-600">Engagement duration</div>
          </div>
        </div>

        <!-- What You Get -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">What you get</h4>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-orange-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Hands-on Claude workshops</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-orange-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Prompt engineering mastery training</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-orange-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Best practices guide and documentation</span>
            </div>
            <div class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-orange-600 mt-0.5 flex-shrink-0" />
              <span class="text-gray-700">Custom use case development</span>
            </div>
          </div>
        </div>

        <!-- How You Get It -->
        <div class="mb-8">
          <h4 class="text-xl font-semibold mb-4 text-gray-900">How you get it</h4>
          <p class="text-gray-700 leading-relaxed">
            Your team participates in intensive hands-on workshops led by Anthropic-certified experts. We start with fundamentals, progress to advanced prompt engineering techniques, and conclude with building custom use cases specific to your business. Each session includes practical exercises, real-world examples, and ongoing support materials for continued learning.
          </p>
        </div>
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
                We combine strategic thinking with hands-on implementation, focusing on rapid results and knowledge transfer. Unlike traditional consultancies, we work alongside your team to build internal capabilities, not just deliver reports.
              {:else if i === 1}
                We establish clear KPIs upfront and track them throughout the engagement. Every recommendation includes ROI projections, and we use rapid pilots to validate assumptions before full-scale investment.
              {:else if i === 2}
                We primarily work with mid-market companies (50-500 employees), but we've successfully partnered with organizations ranging from 20 to 2,000+ employees. What matters most is your commitment to AI transformation.
              {:else if i === 3}
                Yes. Knowledge transfer is built into every engagement. We provide workshops, training sessions, documentation, and hands-on coaching to ensure your team can maintain and evolve the solutions we build together.
              {:else if i === 4}
                Data security is paramount. We follow industry best practices, sign comprehensive NDAs, and can work within your security protocolss. We're experienced with GDPR, HIPAA, and other compliance frameworks.
              {:else if i === 5}
                The initial consultation includes a business assessment, technology audit, opportunity analysis, and preliminary recommendations. It's a no-obligation session designed to determine if we're a good fit.
              {:else if i === 6}
                Absolutely. We're vendor-agnostic and experienced at integrating with existing technology partners. We focus on what's best for your business, not pushing specific vendors.
              {:else if i === 7}
                We offer flexible ongoing support options including monthly retainers, on-demand consulting, and optimization packages. Many clients continue working with us as their AI strategy evolves.
              {/if}
            </div>
          {/if}
        </div>
      {/each}
    </div>
  </section>

  <!-- CTA Section -->
  <section id="contact" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="bg-gradient-to-br from-blue-600 to-purple-600 rounded-3xl p-12 md:p-16 text-center text-white">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Ready to start your AI transformation?</h2>
      <p class="text-xl text-blue-100 mb-10 max-w-2xl mx-auto">
        Schedule a free consultation with our team to discuss your business challenges and explore how AI can drive measurable results.
      </p>
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
        <a href="#consultation" class="inline-flex items-center justify-center gap-2 bg-white text-blue-600 text-base font-medium px-8 py-4 rounded-full hover:bg-blue-50 transition-colors">
          Schedule free consultation
          <ArrowRight size={18} />
        </a>
        <a href="#download" class="inline-flex items-center justify-center gap-2 bg-transparent text-white border-2 border-white text-base font-medium px-8 py-4 rounded-full hover:bg-white/10 transition-colors">
          Download our guide
        </a>
      </div>
      <p class="text-sm text-blue-100 mt-6">No commitment required • 30-minute consultation • Custom strategy roadmap</p>
    </div>
  </section>
</main>
