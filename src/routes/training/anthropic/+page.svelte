<script lang="ts">
  import { ArrowRight, CheckCircle2, Brain, Zap, Target, Award, BookOpen, Code2, Lightbulb, Users, Shield, TrendingUp, Sparkles, Cpu, MessageSquare, GraduationCap } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "What makes Claude different from other AI models?",
    "Do I need programming experience?",
    "How long does the training take?",
    "What will I be able to build after this training?",
    "Is this training suitable for non-technical teams?",
    "Do you provide ongoing support after training?",
    "Can this be customized for our specific use cases?",
    "What's included in the certification?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }

  // Training modules
  const modules = [
    {
      title: "Claude Fundamentals",
      duration: "Day 1-2",
      topics: ["Understanding Claude's capabilities", "API basics and authentication", "Prompt engineering foundations", "Safety and best practices", "Use case identification"]
    },
    {
      title: "Advanced Prompt Engineering",
      duration: "Day 3-4",
      topics: ["Chain-of-thought prompting", "Few-shot learning techniques", "Context optimization", "Output formatting and control", "Error handling strategies"]
    },
    {
      title: "Building with Claude",
      duration: "Day 5-7",
      topics: ["Integration patterns", "Workflow automation", "Custom tool development", "Production deployment", "Performance optimization"]
    },
    {
      title: "Enterprise Applications",
      duration: "Day 8-10",
      topics: ["Security and compliance", "Scaling strategies", "Cost optimization", "Monitoring and analytics", "Team collaboration patterns"]
    }
  ];

  // Key benefits
  const benefits = [
    {
      icon: Brain,
      title: "Master Claude's Capabilities",
      description: "Learn to leverage Claude's advanced reasoning, analysis, and creative capabilities for your specific business needs."
    },
    {
      icon: Code2,
      title: "Hands-On Development",
      description: "Build real applications during training with guided exercises and your own use cases."
    },
    {
      icon: Target,
      title: "Business-Focused Training",
      description: "Every lesson ties directly to business outcomes with ROI-focused examples and case studies."
    },
    {
      icon: Shield,
      title: "Safety & Compliance",
      description: "Understand Anthropic's Constitutional AI approach and implement responsible AI practices."
    },
    {
      icon: Zap,
      title: "Rapid Implementation",
      description: "Go from zero to production-ready solutions in just 2-4 weeks with our accelerated program."
    },
    {
      icon: Users,
      title: "Expert Instructors",
      description: "Learn from certified Anthropic experts with real-world implementation experience."
    }
  ];

  // What you'll build
  const projects = [
    {
      title: "Intelligent Document Processor",
      description: "Build a system that analyzes, summarizes, and extracts insights from complex documents using Claude's advanced comprehension.",
      skills: ["Document analysis", "Information extraction", "Automated summarization"]
    },
    {
      title: "Customer Support Automation",
      description: "Create an AI-powered support system that handles inquiries with context-aware, empathetic responses.",
      skills: ["Conversation design", "Context management", "Response optimization"]
    },
    {
      title: "Code Review Assistant",
      description: "Develop a tool that reviews code, suggests improvements, and explains complex logic using Claude's technical capabilities.",
      skills: ["Code analysis", "Technical writing", "Best practices enforcement"]
    },
    {
      title: "Custom Business Workflow",
      description: "Design and implement an AI workflow tailored to your specific business process and requirements.",
      skills: ["Workflow design", "Integration patterns", "Production deployment"]
    }
  ];

  // Training delivery options
  const deliveryOptions = [
    {
      name: "Intensive Bootcamp",
      duration: "2 weeks",
      format: "Full-time immersive",
      ideal: "Teams ready for rapid transformation",
      features: ["10 days of intensive training", "Daily hands-on labs", "Real project implementation", "Direct instructor access", "Team collaboration exercises"]
    },
    {
      name: "Part-Time Program",
      duration: "4 weeks",
      format: "3 sessions per week",
      ideal: "Teams balancing training with work",
      features: ["Flexible scheduling", "Self-paced labs", "Weekly live sessions", "Recorded content access", "Asynchronous support"]
    },
    {
      name: "Custom Enterprise",
      duration: "Flexible",
      format: "Tailored to your needs",
      ideal: "Large teams with specific requirements",
      features: ["Custom curriculum design", "On-site or remote options", "Industry-specific examples", "Dedicated support team", "Ongoing consultation"]
    }
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
        <a href="/consultancy" class="hover:text-gray-900 transition-colors">Consultancy</a>
        <ArrowRight size={14} />
        <span class="text-gray-900 font-medium">Anthropic AI Training</span>
      </div>

      <!-- Hero Content -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center mb-16">
        <div>
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-gradient-to-r from-orange-50 to-red-50 rounded-full text-sm font-medium text-orange-700 mb-6">
            <Sparkles size={16} />
            Powered by Anthropic Claude
          </div>
          <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black mb-6 leading-[1.1]">
            Master Claude AI with expert-led training
          </h1>
          <p class="text-xl text-gray-600 leading-relaxed mb-8">
            Transform your team into Claude AI experts through our comprehensive, hands-on training program. Build production-ready applications with Anthropic's most advanced AI model.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#enroll" class="inline-flex items-center justify-center gap-2 bg-black text-white text-base font-medium px-8 py-4 rounded-full hover:bg-gray-800 transition-colors">
              Enroll your team
              <ArrowRight size={18} />
            </a>
            <a href="#curriculum" class="inline-flex items-center justify-center gap-2 bg-white text-black border-2 border-gray-200 text-base font-medium px-8 py-4 rounded-full hover:bg-gray-50 transition-colors">
              View curriculum
            </a>
          </div>
        </div>

        <!-- Hero Image -->
        <div class="relative">
          <div class="aspect-[4/3] rounded-3xl overflow-hidden shadow-2xl bg-gradient-to-br from-orange-100 to-red-100 flex items-center justify-center">
            <img src="/generated/image-corporate-training-session-with-diverse--1770142833958-0.webp" alt="Anthropic Claude AI Training" class="w-full h-full object-cover" />
          </div>
          <!-- Floating Stats Card -->
          <div class="absolute -bottom-6 -left-6 bg-white rounded-2xl shadow-xl p-6 border border-gray-100">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center">
                <GraduationCap size={24} class="text-orange-600" />
              </div>
              <div>
                <div class="text-2xl font-bold text-gray-900">500+</div>
                <div class="text-sm text-gray-600">Developers trained</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Trust Indicators -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 pt-12 border-t border-gray-100">
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">2-4 weeks</div>
          <div class="text-sm text-gray-600">To production ready</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">100%</div>
          <div class="text-sm text-gray-600">Hands-on learning</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">4.9/5</div>
          <div class="text-sm text-gray-600">Training rating</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">Certified</div>
          <div class="text-sm text-gray-600">Anthropic experts</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Why Claude Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-orange-50 to-red-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Why train on Claude?</h2>
      <p class="text-xl text-gray-600">
        Claude represents the cutting edge of AI safety, capability, and business value. Here's why leading companies choose Claude for their AI initiatives.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-orange-100 rounded-2xl flex items-center justify-center mb-6">
          <Brain size={28} class="text-orange-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Superior Reasoning</h3>
        <p class="text-gray-600 leading-relaxed">
          Claude excels at complex reasoning, analysis, and nuanced understanding. Perfect for sophisticated business applications requiring deep comprehension and thoughtful responses.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-red-100 rounded-2xl flex items-center justify-center mb-6">
          <Shield size={28} class="text-red-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Constitutional AI</h3>
        <p class="text-gray-600 leading-relaxed">
          Built with safety at its core through Anthropic's Constitutional AI approach. Reduce risks and ensure responsible AI deployment in your organization.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-purple-100 rounded-2xl flex items-center justify-center mb-6">
          <Cpu size={28} class="text-purple-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Extended Context</h3>
        <p class="text-gray-600 leading-relaxed">
          Process massive amounts of information with Claude's industry-leading context window. Analyze entire codebases, documents, and datasets in a single conversation.
        </p>
      </div>
    </div>
  </section>

  <!-- Training Benefits -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">What you'll gain</h2>
      <p class="text-xl text-gray-600">
        Our training program delivers practical skills and strategic insights that translate directly into business value.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each benefits as benefit}
        <div class="bg-white rounded-2xl p-6 shadow-sm border border-gray-200 hover:shadow-md transition-shadow">
          <div class="w-12 h-12 bg-orange-100 rounded-xl flex items-center justify-center mb-4">
            <svelte:component this={benefit.icon} size={24} class="text-orange-600" />
          </div>
          <h3 class="text-xl font-semibold mb-3">{benefit.title}</h3>
          <p class="text-sm text-gray-600 leading-relaxed">{benefit.description}</p>
        </div>
      {/each}
    </div>
  </section>

  <!-- Curriculum Section -->
  <section id="curriculum" class="max-w-[1400px] mx-auto px-6 py-24 bg-gray-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Comprehensive curriculum</h2>
      <p class="text-xl text-gray-600">
        A structured learning path that takes you from Claude basics to production deployment in just 2-4 weeks.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      {#each modules as module, i}
        <div class="bg-white rounded-3xl p-8 shadow-sm border border-gray-200">
          <div class="flex items-center justify-between mb-6">
            <div class="inline-flex items-center gap-2 px-3 py-1 bg-orange-100 rounded-full text-xs font-medium text-orange-700">
              Module {i + 1}
            </div>
            <div class="text-sm font-medium text-gray-500">{module.duration}</div>
          </div>
          <h3 class="text-2xl font-semibold mb-6">{module.title}</h3>
          <div class="space-y-3">
            {#each module.topics as topic}
              <div class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-sm text-gray-700">{topic}</span>
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- What You'll Build -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Real projects, real skills</h2>
      <p class="text-xl text-gray-600">
        Build production-ready applications during the training program. You'll leave with working solutions and the skills to create more.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      {#each projects as project}
        <div class="bg-gradient-to-br from-white to-gray-50 rounded-2xl p-8 border border-gray-200 shadow-sm hover:shadow-md transition-shadow">
          <h3 class="text-2xl font-semibold mb-4">{project.title}</h3>
          <p class="text-gray-600 leading-relaxed mb-6">{project.description}</p>
          <div class="flex flex-wrap gap-2">
            {#each project.skills as skill}
              <span class="px-3 py-1 bg-orange-100 text-orange-700 text-xs font-medium rounded-full">{skill}</span>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Training Delivery Options -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-gray-50 to-orange-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Flexible training formats</h2>
      <p class="text-xl text-gray-600">
        Choose the delivery format that works best for your team's schedule and learning style.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      {#each deliveryOptions as option}
        <div class="bg-white rounded-3xl p-8 shadow-lg border border-gray-200 flex flex-col">
          <div class="mb-6">
            <h3 class="text-2xl font-semibold mb-2">{option.name}</h3>
            <div class="flex items-center gap-4 text-sm text-gray-600 mb-1">
              <span class="font-medium">{option.duration}</span>
              <span>•</span>
              <span>{option.format}</span>
            </div>
            <p class="text-sm text-gray-500 mt-2">
              <span class="font-medium text-gray-700">Ideal for:</span> {option.ideal}
            </p>
          </div>
          <div class="space-y-3 flex-grow mb-8">
            {#each option.features as feature}
              <div class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-sm text-gray-700">{feature}</span>
              </div>
            {/each}
          </div>
          <a href="#enroll" class="w-full inline-flex items-center justify-center gap-2 bg-black text-white text-sm font-medium px-6 py-3 rounded-full hover:bg-gray-800 transition-colors">
            Get started
            <ArrowRight size={16} />
          </a>
        </div>
      {/each}
    </div>
  </section>

  <!-- Instructor Expertise -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
      <div>
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Learn from certified Anthropic experts</h2>
        <p class="text-xl text-gray-600 leading-relaxed mb-8">
          Our instructors are certified Anthropic experts with extensive real-world experience building production AI systems with Claude.
        </p>
        
        <div class="space-y-6">
          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-orange-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <Award size={20} class="text-orange-600" />
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Certified Expertise</h3>
              <p class="text-gray-600 text-sm leading-relaxed">All instructors are certified by Anthropic and maintain active development practices with Claude.</p>
            </div>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <Briefcase size={20} class="text-purple-600" />
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Real-World Experience</h3>
              <p class="text-gray-600 text-sm leading-relaxed">Our team has built and deployed Claude-powered solutions across multiple industries and use cases.</p>
            </div>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <Users size={20} class="text-blue-600" />
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Dedicated Support</h3>
              <p class="text-gray-600 text-sm leading-relaxed">Small class sizes ensure personalized attention and support throughout your learning journey.</p>
            </div>
          </div>
        </div>
      </div>

      <div class="relative">
        <div class="aspect-[3/4] rounded-3xl overflow-hidden shadow-2xl">
          <img src="/generated/image-confident-female-business-trainer-presen-1770142839445-2.webp" alt="Expert Instructor" class="w-full h-full object-cover" />
        </div>
      </div>
    </div>
  </section>

  <!-- Success Stories -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-purple-50 to-pink-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Training success stories</h2>
      <p class="text-xl text-gray-600">
        See how teams are transforming their capabilities with our Anthropic-focused training.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Success Story 1 -->
      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
            <Code2 size={24} class="text-blue-600" />
          </div>
          <div>
            <div class="font-semibold text-gray-900">SaaS Technology Company</div>
            <div class="text-sm text-gray-500">15-person engineering team</div>
          </div>
        </div>
        <p class="text-gray-700 leading-relaxed mb-6 italic">
          "Within 3 weeks of completing the training, our team had built and deployed three Claude-powered features. The hands-on approach and expert guidance made all the difference."
        </p>
        <div class="grid grid-cols-3 gap-4 pt-6 border-t border-gray-100">
          <div>
            <div class="text-2xl font-bold text-gray-900">3</div>
            <div class="text-xs text-gray-600">Features launched</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">60%</div>
            <div class="text-xs text-gray-600">Faster development</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">$200K</div>
            <div class="text-xs text-gray-600">Annual savings</div>
          </div>
        </div>
      </div>

      <!-- Success Story 2 -->
      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center">
            <TrendingUp size={24} class="text-green-600" />
          </div>
          <div>
            <div class="font-semibold text-gray-900">Financial Services Firm</div>
            <div class="text-sm text-gray-500">25-person operations team</div>
          </div>
        </div>
        <p class="text-gray-700 leading-relaxed mb-6 italic">
          "The training gave our non-technical team the confidence to build AI-powered workflows. We've automated processes that used to take hours and now complete in minutes."
        </p>
        <div class="grid grid-cols-3 gap-4 pt-6 border-t border-gray-100">
          <div>
            <div class="text-2xl font-bold text-gray-900">12</div>
            <div class="text-xs text-gray-600">Workflows automated</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">85%</div>
            <div class="text-xs text-gray-600">Time savings</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">4.9/5</div>
            <div class="text-xs text-gray-600">Team satisfaction</div>
          </div>
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
                Claude is built with Constitutional AI, making it safer and more aligned with human values. It excels at nuanced reasoning, has an industry-leading context window, and provides more thoughtful, detailed responses. Claude is particularly strong at analysis, writing, and complex problem-solving.
              {:else if i === 1}
                No programming experience is required for our foundational modules. We offer tracks for both technical and non-technical teams. However, some advanced modules do benefit from basic programming knowledge, which we can provide as part of the training.
              {:else if i === 2}
                Our intensive bootcamp runs for 2 weeks full-time, while our part-time program spans 4 weeks with flexible scheduling. Custom enterprise programs can be tailored to your timeline and needs.
              {:else if i === 3}
                You'll be able to build production-ready AI applications including document processors, customer support systems, code assistants, and custom business workflows. You'll have working projects to take back to your organization.
              {:else if i === 4}
                Absolutely. We have specific tracks designed for non-technical teams focusing on prompt engineering, workflow design, and practical applications without requiring coding skills.
              {:else if i === 5}
                Yes. All training includes 30 days of post-training support via email and office hours. We also offer optional ongoing support packages and advanced workshops for continued learning.
              {:else if i === 6}
                Yes. We specialize in customizing the training to your specific industry and use cases. All programs include time to work on your actual business challenges with instructor guidance.
              {:else if i === 7}
                Participants receive a certificate of completion from our program. We also provide documentation of skills acquired and projects completed, which can be used for professional development records.
              {/if}
            </div>
          {/if}
        </div>
      {/each}
    </div>
  </section>

  <!-- CTA Section -->
  <section id="enroll" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="bg-gradient-to-br from-orange-600 to-red-600 rounded-3xl p-12 md:p-16 text-center text-white">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Ready to master Claude AI?</h2>
      <p class="text-xl text-orange-100 mb-10 max-w-2xl mx-auto">
        Transform your team's capabilities with our comprehensive Anthropic-focused training program. Limited seats available for upcoming cohorts.
      </p>
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
        <a href="/contact" class="inline-flex items-center justify-center gap-2 bg-white text-orange-600 text-base font-medium px-8 py-4 rounded-full hover:bg-orange-50 transition-colors">
          Enroll your team
          <ArrowRight size={18} />
        </a>
        <a href="#curriculum" class="inline-flex items-center justify-center gap-2 bg-transparent text-white border-2 border-white text-base font-medium px-8 py-4 rounded-full hover:bg-white/10 transition-colors">
          Download syllabus
        </a>
      </div>
      <p class="text-sm text-orange-100 mt-6">Next cohort starts soon • Small class sizes • Satisfaction guaranteed</p>
    </div>
  </section>
</main>
