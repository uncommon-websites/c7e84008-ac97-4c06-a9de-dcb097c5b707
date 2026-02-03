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

  <!-- Our Approach Section -->
  <section id="approach" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Our consultancy approach</h2>
      <p class="text-xl text-gray-600">
        We combine strategic thinking with hands-on execution to deliver AI solutions that actually work for your business.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
      <!-- Approach 1 -->
      <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-3xl p-8 border border-blue-100">
        <div class="w-14 h-14 bg-blue-600 rounded-2xl flex items-center justify-center mb-6">
          <Target size={28} class="text-white" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Business-First Thinking</h3>
        <p class="text-gray-700 leading-relaxed mb-6">
          We start with your business objectives, not the technology. Every recommendation is tied to measurable business outcomes and ROI projections.
        </p>
        <ul class="space-y-2 text-sm text-gray-700">
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
            <span>Revenue impact analysis</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
            <span>Cost-benefit modeling</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-blue-600 mt-0.5 flex-shrink-0" />
            <span>Risk assessment</span>
          </li>
        </ul>
      </div>

      <!-- Approach 2 -->
      <div class="bg-gradient-to-br from-purple-50 to-pink-50 rounded-3xl p-8 border border-purple-100">
        <div class="w-14 h-14 bg-purple-600 rounded-2xl flex items-center justify-center mb-6">
          <Users size={28} class="text-white" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Collaborative Partnership</h3>
        <p class="text-gray-700 leading-relaxed mb-6">
          We work alongside your team, transferring knowledge and building internal capabilities. You're not just getting a solution — you're building expertise.
        </p>
        <ul class="space-y-2 text-sm text-gray-700">
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
            <span>Team training & workshops</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
            <span>Knowledge transfer sessions</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
            <span>Documentation & playbooks</span>
          </li>
        </ul>
      </div>

      <!-- Approach 3 -->
      <div class="bg-gradient-to-br from-green-50 to-emerald-50 rounded-3xl p-8 border border-green-100">
        <div class="w-14 h-14 bg-green-600 rounded-2xl flex items-center justify-center mb-6">
          <Zap size={28} class="text-white" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Rapid Implementation</h3>
        <p class="text-gray-700 leading-relaxed mb-6">
          No endless planning cycles. We deliver working solutions quickly through our proven rapid pilot methodology, then iterate based on real results.
        </p>
        <ul class="space-y-2 text-sm text-gray-700">
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
            <span>2-4 week pilot programs</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
            <span>Agile development cycles</span>
          </li>
          <li class="flex items-start gap-2">
            <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
            <span>Continuous optimization</span>
          </li>
        </ul>
      </div>
    </div>
  </section>

  <!-- Engagement Models Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gray-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Flexible engagement models</h2>
      <p class="text-xl text-gray-600">
        Choose the partnership model that fits your needs, timeline, and budget.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
      {#each engagementModels as model, i}
        <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200 hover:shadow-lg transition-shadow flex flex-col">
          <div class="flex items-center justify-between mb-6">
            <div class="w-12 h-12 bg-gray-100 rounded-xl flex items-center justify-center">
              <span class="text-xl font-bold text-gray-900">{i + 1}</span>
            </div>
            <div class="text-sm font-medium text-gray-500">{model.duration}</div>
          </div>
          <h3 class="text-2xl font-semibold mb-3">{model.title}</h3>
          <p class="text-sm text-gray-600 mb-6 pb-6 border-b border-gray-100">
            <span class="font-medium text-gray-700">Ideal for:</span> {model.ideal}
          </p>
          <div class="space-y-3 flex-grow">
            <div class="text-sm font-semibold text-gray-900 mb-3">Key deliverables:</div>
            {#each model.deliverables as deliverable}
              <div class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-sm text-gray-700">{deliverable}</span>
              </div>
            {/each}
          </div>
          <a href={i === 3 ? '/training/anthropic' : '#contact'} class="mt-8 w-full inline-flex items-center justify-center gap-2 bg-black text-white text-sm font-medium px-6 py-3 rounded-full hover:bg-gray-800 transition-colors">
            Learn more
            <ArrowRight size={16} />
          </a>
        </div>
      {/each}
    </div>
  </section>

  <!-- Industry Expertise Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Industry expertise</h2>
      <p class="text-xl text-gray-600">
        Deep domain knowledge across multiple industries ensures we understand your unique challenges and opportunities.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      {#each industries as industry}
        <div class="bg-white rounded-2xl p-6 border border-gray-200 hover:border-gray-300 transition-all hover:shadow-md">
          <div class={[
            'w-12 h-12 rounded-xl flex items-center justify-center mb-4',
            industry.color === 'blue' ? 'bg-blue-100' : '',
            industry.color === 'green' ? 'bg-green-100' : '',
            industry.color === 'purple' ? 'bg-purple-100' : '',
            industry.color === 'orange' ? 'bg-orange-100' : '',
            industry.color === 'indigo' ? 'bg-indigo-100' : '',
            industry.color === 'red' ? 'bg-red-100' : ''
          ]}>
            <svelte:component this={industry.icon} size={24} class={[
              industry.color === 'blue' ? 'text-blue-600' : '',
              industry.color === 'green' ? 'text-green-600' : '',
              industry.color === 'purple' ? 'text-purple-600' : '',
              industry.color === 'orange' ? 'text-orange-600' : '',
              industry.color === 'indigo' ? 'text-indigo-600' : '',
              industry.color === 'red' ? 'text-red-600' : ''
            ]} />
          </div>
          <h3 class="text-xl font-semibold mb-3">{industry.name}</h3>
          <p class="text-sm text-gray-600 leading-relaxed">{industry.focus}</p>
        </div>
      {/each}
    </div>
  </section>

  <!-- Consultancy Process Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-gray-50 to-blue-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">How we work with you</h2>
      <p class="text-xl text-gray-600">
        A proven methodology that takes you from strategy to implementation with confidence.
      </p>
    </div>

    <div class="relative">
      <!-- Timeline Line -->
      <div class="hidden md:block absolute left-1/2 top-0 bottom-0 w-0.5 bg-gradient-to-b from-blue-200 via-purple-200 to-green-200 transform -translate-x-1/2"></div>

      <div class="space-y-16">
        <!-- Phase 1 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div class="md:text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-blue-100 rounded-full text-sm font-medium text-blue-700 mb-4">
              <Calendar size={16} />
              Week 1-2
            </div>
            <h3 class="text-2xl font-semibold mb-3">Discovery & Assessment</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
              We immerse ourselves in your business, understanding your workflows, challenges, and opportunities through stakeholder interviews and data analysis.
            </p>
            <ul class="space-y-2 text-sm text-gray-700">
              <li class="flex items-end md:justify-end gap-2">
                <span>Stakeholder interviews</span>
                <CheckCircle2 size={16} class="text-blue-600 flex-shrink-0" />
              </li>
              <li class="flex items-end md:justify-end gap-2">
                <span>Process mapping</span>
                <CheckCircle2 size={16} class="text-blue-600 flex-shrink-0" />
              </li>
              <li class="flex items-end md:justify-end gap-2">
                <span>Technology audit</span>
                <CheckCircle2 size={16} class="text-blue-600 flex-shrink-0" />
              </li>
            </ul>
          </div>
          <div class="relative">
            <div class="hidden md:block absolute -left-4 top-1/2 transform -translate-y-1/2 w-8 h-8 bg-blue-600 rounded-full border-4 border-white shadow-lg z-10"></div>
            <div class="bg-white rounded-2xl p-6 shadow-lg border border-gray-200">
              <div class="flex items-center gap-3 mb-4">
                <FileText size={24} class="text-blue-600" />
                <span class="font-semibold">Deliverable</span>
              </div>
              <p class="text-sm text-gray-700">Comprehensive assessment report with opportunity analysis and preliminary recommendations</p>
            </div>
          </div>
        </div>

        <!-- Phase 2 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div class="md:order-2">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-purple-100 rounded-full text-sm font-medium text-purple-700 mb-4">
              <Calendar size={16} />
              Week 3-4
            </div>
            <h3 class="text-2xl font-semibold mb-3">Strategy Development</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
              We craft a detailed AI strategy aligned with your business goals, including technology recommendations, implementation roadmap, and ROI projections.
            </p>
            <ul class="space-y-2 text-sm text-gray-700">
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
                <span>Strategic roadmap creation</span>
              </li>
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
                <span>Technology stack recommendations</span>
              </li>
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-purple-600 mt-0.5 flex-shrink-0" />
                <span>ROI modeling</span>
              </li>
            </ul>
          </div>
          <div class="md:order-1 relative">
            <div class="hidden md:block absolute -right-4 top-1/2 transform -translate-y-1/2 w-8 h-8 bg-purple-600 rounded-full border-4 border-white shadow-lg z-10"></div>
            <div class="bg-white rounded-2xl p-6 shadow-lg border border-gray-200">
              <div class="flex items-center gap-3 mb-4">
                <LineChart size={24} class="text-purple-600" />
                <span class="font-semibold">Deliverable</span>
              </div>
              <p class="text-sm text-gray-700">AI transformation strategy with detailed roadmap, budget estimates, and success metrics</p>
            </div>
          </div>
        </div>

        <!-- Phase 3 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div class="md:text-right">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-green-100 rounded-full text-sm font-medium text-green-700 mb-4">
              <Calendar size={16} />
              Week 5-8
            </div>
            <h3 class="text-2xl font-semibold mb-3">Pilot Implementation</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
              We launch a focused pilot project to validate the strategy, demonstrate value, and gather real-world performance data before full-scale deployment.
            </p>
            <ul class="space-y-2 text-sm text-gray-700">
              <li class="flex items-end md:justify-end gap-2">
                <span>Rapid prototype development</span>
                <CheckCircle2 size={16} class="text-green-600 flex-shrink-0" />
              </li>
              <li class="flex items-end md:justify-end gap-2">
                <span>User testing & feedback</span>
                <CheckCircle2 size={16} class="text-green-600 flex-shrink-0" />
              </li>
              <li class="flex items-end md:justify-end gap-2">
                <span>Performance measurement</span>
                <CheckCircle2 size={16} class="text-green-600 flex-shrink-0" />
              </li>
            </ul>
          </div>
          <div class="relative">
            <div class="hidden md:block absolute -left-4 top-1/2 transform -translate-y-1/2 w-8 h-8 bg-green-600 rounded-full border-4 border-white shadow-lg z-10"></div>
            <div class="bg-white rounded-2xl p-6 shadow-lg border border-gray-200">
              <div class="flex items-center gap-3 mb-4">
                <Zap size={24} class="text-green-600" />
                <span class="font-semibold">Deliverable</span>
              </div>
              <p class="text-sm text-gray-700">Working pilot solution with performance metrics, user feedback, and scale-up recommendations</p>
            </div>
          </div>
        </div>

        <!-- Phase 4 -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
          <div class="md:order-2">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-orange-100 rounded-full text-sm font-medium text-orange-700 mb-4">
              <Calendar size={16} />
              Ongoing
            </div>
            <h3 class="text-2xl font-semibold mb-3">Scale & Optimize</h3>
            <p class="text-gray-600 leading-relaxed mb-4">
              We expand successful pilots across your organization, continuously optimizing performance and providing ongoing support as your AI capabilities mature.
            </p>
            <ul class="space-y-2 text-sm text-gray-700">
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-orange-600 mt-0.5 flex-shrink-0" />
                <span>Full deployment support</span>
              </li>
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-orange-600 mt-0.5 flex-shrink-0" />
                <span>Team training programs</span>
              </li>
              <li class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-orange-600 mt-0.5 flex-shrink-0" />
                <span>Continuous improvement</span>
              </li>
            </ul>
          </div>
          <div class="md:order-1 relative">
            <div class="hidden md:block absolute -right-4 top-1/2 transform -translate-y-1/2 w-8 h-8 bg-orange-600 rounded-full border-4 border-white shadow-lg z-10"></div>
            <div class="bg-white rounded-2xl p-6 shadow-lg border border-gray-200">
              <div class="flex items-center gap-3 mb-4">
                <TrendingUp size={24} class="text-orange-600" />
                <span class="font-semibold">Deliverable</span>
              </div>
              <p class="text-sm text-gray-700">Production-ready solution with documentation, training materials, and ongoing optimization support</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Why Choose Our Consultancy -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Why choose Flowgrid consultancy</h2>
      <p class="text-xl text-gray-600">
        We bring the perfect blend of strategic thinking, technical expertise, and business acumen.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
        <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center mb-6">
          <Shield size={24} class="text-blue-600" />
        </div>
        <h3 class="text-xl font-semibold mb-3">Proven Track Record</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
          50+ successful implementations across multiple industries with an average ROI of 300% within the first year.
        </p>
        <div class="flex items-center gap-2 text-sm text-blue-600 font-medium">
          <span>View case studies</span>
          <ArrowRight size={16} />
        </div>
      </div>

      <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
        <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center mb-6">
          <Users size={24} class="text-purple-600" />
        </div>
        <h3 class="text-xl font-semibold mb-3">Expert Team</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
          Our consultants combine deep AI expertise with real-world business experience from Fortune 500 companies and high-growth startups.
        </p>
        <div class="flex items-center gap-2 text-sm text-purple-600 font-medium">
          <span>Meet the team</span>
          <ArrowRight size={16} />
        </div>
      </div>

      <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
        <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center mb-6">
          <Target size={24} class="text-green-600" />
        </div>
        <h3 class="text-xl font-semibold mb-3">Business-Focused Approach</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
          We prioritize business outcomes over technical complexity. Every recommendation is tied to measurable impact on your bottom line.
        </p>
        <div class="flex items-center gap-2 text-sm text-green-600 font-medium">
          <span>Our methodology</span>
          <ArrowRight size={16} />
        </div>
      </div>

      <div class="bg-white rounded-2xl p-8 border border-gray-200 shadow-sm">
        <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center mb-6">
          <MessageSquare size={24} class="text-orange-600" />
        </div>
        <h3 class="text-xl font-semibold mb-3">Ongoing Partnership</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
          We don't disappear after implementation. Our team provides continuous support, optimization, and strategic guidance as your needs evolve.
        </p>
        <div class="flex items-center gap-2 text-sm text-orange-600 font-medium">
          <span>Support options</span>
          <ArrowRight size={16} />
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
                Data security is paramount. We follow industry best practices, sign comprehensive NDAs, and can work within your security protocols. We're experienced with GDPR, HIPAA, and other compliance frameworks.
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
