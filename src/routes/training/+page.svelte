<script lang="ts">
  import { ArrowRight, CheckCircle2, Users, Zap, Target, TrendingUp, Clock, Shield, Award, BookOpen, Brain, Lightbulb, GraduationCap, BarChart3, Code2, Briefcase, Calendar } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "Who should attend the AI training programs?",
    "What is the typical duration of a training program?",
    "Do you offer custom training for specific industries?",
    "What level of technical knowledge is required?",
    "Can training be delivered remotely?",
    "Do you provide certification upon completion?",
    "How do you measure training effectiveness?",
    "What ongoing support is available after training?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }

  // Training programs
  const trainingPrograms = [
    {
      title: "AI Fundamentals for Leaders",
      duration: "2 days",
      audience: "C-suite, VPs, Directors",
      level: "Executive",
      topics: ["AI strategy & business value", "Use case identification", "Risk & governance", "ROI evaluation", "Change management"]
    },
    {
      title: "AI Implementation for Teams",
      duration: "5 days",
      audience: "Operations, Product, Engineering",
      level: "Practitioner",
      topics: ["Workflow automation", "Tool selection", "Integration strategies", "Performance monitoring", "Best practices"]
    },
    {
      title: "Advanced AI Development",
      duration: "10 days",
      audience: "Technical teams, Data scientists",
      level: "Technical",
      topics: ["Model development", "Fine-tuning & optimization", "Production deployment", "MLOps practices", "Advanced architectures"]
    }
  ];

  // Learning outcomes
  const outcomes = [
    {
      icon: Brain,
      title: "Strategic AI Understanding",
      description: "Develop a comprehensive understanding of AI capabilities, limitations, and strategic applications for your business context."
    },
    {
      icon: Target,
      title: "Practical Implementation Skills",
      description: "Gain hands-on experience with AI tools and frameworks through real-world exercises and case studies."
    },
    {
      icon: Shield,
      title: "Risk Management Expertise",
      description: "Learn to identify and mitigate AI risks including bias, security concerns, and compliance requirements."
    },
    {
      icon: TrendingUp,
      title: "ROI Measurement",
      description: "Master frameworks for evaluating AI investments and demonstrating business value to stakeholders."
    },
    {
      icon: Users,
      title: "Change Leadership",
      description: "Build skills to lead AI transformation initiatives and drive adoption across your organization."
    },
    {
      icon: Lightbulb,
      title: "Innovation Mindset",
      description: "Cultivate the ability to identify AI opportunities and develop innovative solutions for business challenges."
    }
  ];

  // Training delivery methods
  const deliveryMethods = [
    {
      name: "In-Person Workshops",
      icon: Users,
      description: "Immersive on-site training at your location with hands-on exercises and team collaboration",
      benefits: ["Maximum engagement", "Team building", "Custom environment", "Direct interaction"]
    },
    {
      name: "Virtual Instructor-Led",
      icon: BookOpen,
      description: "Live online sessions with expert instructors, interactive exercises, and real-time Q&A",
      benefits: ["Location flexibility", "Cost effective", "Recorded sessions", "Global accessibility"]
    },
    {
      name: "Hybrid Programs",
      icon: Zap,
      description: "Combination of virtual learning and in-person workshops for optimal flexibility and impact",
      benefits: ["Best of both worlds", "Flexible scheduling", "Reduced travel", "Sustained engagement"]
    },
    {
      name: "Custom Bootcamps",
      icon: Target,
      description: "Intensive multi-day programs tailored to your specific use cases and business objectives",
      benefits: ["Rapid skill building", "Focused outcomes", "Team alignment", "Immediate application"]
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
        <span class="text-gray-900 font-medium">AI Training</span>
      </div>

      <!-- Hero Content -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center mb-16">
        <div>
          <div class="inline-flex items-center gap-2 px-4 py-2 bg-purple-50 rounded-full text-sm font-medium text-purple-700 mb-6">
            <GraduationCap size={16} />
            Corporate AI Training
          </div>
          <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black mb-6 leading-[1.1]">
            Empower your team with enterprise AI expertise
          </h1>
          <p class="text-xl text-gray-600 leading-relaxed mb-8">
            Transform your organization's AI capabilities through comprehensive training programs designed for business leaders, operations teams, and technical professionals.
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#programs" class="inline-flex items-center justify-center gap-2 bg-black text-white text-base font-medium px-8 py-4 rounded-full hover:bg-gray-800 transition-colors">
              Explore programs
              <ArrowRight size={18} />
            </a>
            <a href="#contact" class="inline-flex items-center justify-center gap-2 bg-white text-black border-2 border-gray-200 text-base font-medium px-8 py-4 rounded-full hover:bg-gray-50 transition-colors">
              Request consultation
            </a>
          </div>
        </div>

        <!-- Hero Image -->
        <div class="relative">
          <div class="aspect-[16/9] rounded-3xl overflow-hidden shadow-2xl">
            <img src="/generated/image-corporate-training-session-with-diverse--1770142833958-0.webp" alt="Corporate AI Training Session" class="w-full h-full object-cover" />
          </div>
          <!-- Floating Stats Card -->
          <div class="absolute -bottom-6 -left-6 bg-white rounded-2xl shadow-xl p-6 border border-gray-100">
            <div class="flex items-center gap-4">
              <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center">
                <Users size={24} class="text-purple-600" />
              </div>
              <div>
                <div class="text-2xl font-bold text-gray-900">2,500+</div>
                <div class="text-sm text-gray-600">Professionals trained</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Trust Indicators -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 pt-12 border-t border-gray-100">
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">95%</div>
          <div class="text-sm text-gray-600">Satisfaction rate</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">50+</div>
          <div class="text-sm text-gray-600">Companies trained</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">15+</div>
          <div class="text-sm text-gray-600">Training programs</div>
        </div>
        <div class="text-center">
          <div class="text-3xl font-bold text-gray-900 mb-1">4.8/5</div>
          <div class="text-sm text-gray-600">Average rating</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Why AI Training Matters -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-blue-50 to-indigo-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Why AI training is critical for your business</h2>
      <p class="text-xl text-gray-600">
        The AI skills gap is the biggest barrier to successful AI adoption. Equip your team with the knowledge and capabilities to drive real transformation.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-blue-100 rounded-2xl flex items-center justify-center mb-6">
          <BarChart3 size={28} class="text-blue-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Bridge the Skills Gap</h3>
        <p class="text-gray-600 leading-relaxed">
          85% of companies report AI skills shortages. Our training programs rapidly upskill your team, eliminating the need for expensive external hires while building internal AI capabilities.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-purple-100 rounded-2xl flex items-center justify-center mb-6">
          <TrendingUp size={28} class="text-purple-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Accelerate ROI</h3>
        <p class="text-gray-600 leading-relaxed">
          Trained teams implement AI solutions 3x faster and achieve better outcomes. Reduce implementation timelines from months to weeks with proper training and knowledge transfer.
        </p>
      </div>

      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="w-14 h-14 bg-green-100 rounded-2xl flex items-center justify-center mb-6">
          <Shield size={28} class="text-green-600" />
        </div>
        <h3 class="text-2xl font-semibold mb-4">Mitigate Risk</h3>
        <p class="text-gray-600 leading-relaxed">
          Proper AI training ensures your team understands governance, ethics, and compliance requirements — reducing costly mistakes and protecting your organization from AI-related risks.
        </p>
      </div>
    </div>
  </section>

  <!-- Training Programs -->
  <section id="programs" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Comprehensive training programs</h2>
      <p class="text-xl text-gray-600">
        From executive strategy to technical implementation, we offer training programs tailored to every role and skill level in your organization.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
      {#each trainingPrograms as program, i}
        <div class="bg-white rounded-3xl p-8 shadow-lg border border-gray-200 hover:shadow-xl transition-shadow">
          <div class="flex items-center justify-between mb-6">
            <div class="inline-flex items-center gap-2 px-3 py-1 bg-gray-100 rounded-full text-xs font-medium text-gray-700">
              {program.level}
            </div>
            <div class="text-sm font-medium text-gray-500">{program.duration}</div>
          </div>
          <h3 class="text-2xl font-semibold mb-3">{program.title}</h3>
          <p class="text-sm text-gray-600 mb-6 pb-6 border-b border-gray-100">
            <span class="font-medium text-gray-700">Target audience:</span> {program.audience}
          </p>
          <div class="space-y-3 mb-8">
            <div class="text-sm font-semibold text-gray-900 mb-3">Key topics covered:</div>
            {#each program.topics as topic}
              <div class="flex items-start gap-2">
                <CheckCircle2 size={16} class="text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-sm text-gray-700">{topic}</span>
              </div>
            {/each}
          </div>
          <a href="#contact" class="w-full inline-flex items-center justify-center gap-2 bg-black text-white text-sm font-medium px-6 py-3 rounded-full hover:bg-gray-800 transition-colors">
            Learn more
            <ArrowRight size={16} />
          </a>
        </div>
      {/each}
    </div>
  </section>

  <!-- Learning Outcomes -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gray-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">What your team will learn</h2>
      <p class="text-xl text-gray-600">
        Our training programs deliver practical skills and strategic insights that translate directly into business value.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each outcomes as outcome}
        <div class="bg-white rounded-2xl p-6 shadow-sm border border-gray-200">
          <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center mb-4">
            <svelte:component this={outcome.icon} size={24} class="text-blue-600" />
          </div>
          <h3 class="text-xl font-semibold mb-3">{outcome.title}</h3>
          <p class="text-sm text-gray-600 leading-relaxed">{outcome.description}</p>
        </div>
      {/each}
    </div>
  </section>

  <!-- Training Delivery Methods -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Flexible training delivery</h2>
      <p class="text-xl text-gray-600">
        Choose the delivery format that works best for your team's schedule, location, and learning preferences.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      {#each deliveryMethods as method}
        <div class="bg-gradient-to-br from-white to-gray-50 rounded-2xl p-8 border border-gray-200 shadow-sm hover:shadow-md transition-shadow">
          <div class="flex items-start gap-4 mb-6">
            <div class="w-14 h-14 bg-purple-100 rounded-2xl flex items-center justify-center flex-shrink-0">
              <svelte:component this={method.icon} size={28} class="text-purple-600" />
            </div>
            <div>
              <h3 class="text-2xl font-semibold mb-2">{method.name}</h3>
              <p class="text-gray-600 leading-relaxed">{method.description}</p>
            </div>
          </div>
          <div class="grid grid-cols-2 gap-3">
            {#each method.benefits as benefit}
              <div class="flex items-center gap-2">
                <CheckCircle2 size={14} class="text-green-600 flex-shrink-0" />
                <span class="text-xs text-gray-700">{benefit}</span>
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Training Approach -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
      <div>
        <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Our training methodology</h2>
        <p class="text-xl text-gray-600 leading-relaxed mb-8">
          We combine theoretical foundations with hands-on practice, ensuring your team can immediately apply what they learn to real business challenges.
        </p>
        
        <div class="space-y-6">
          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <span class="text-lg font-bold text-blue-600">1</span>
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Interactive Learning</h3>
              <p class="text-gray-600 text-sm leading-relaxed">Live exercises, group discussions, and real-world case studies keep participants engaged and facilitate deeper understanding.</p>
            </div>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-purple-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <span class="text-lg font-bold text-purple-600">2</span>
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Hands-On Practice</h3>
              <p class="text-gray-600 text-sm leading-relaxed">Participants work with actual AI tools and platforms, building practical skills through guided exercises and projects.</p>
            </div>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-green-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <span class="text-lg font-bold text-green-600">3</span>
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Custom Scenarios</h3>
              <p class="text-gray-600 text-sm leading-relaxed">We tailor examples and exercises to your industry and specific business challenges for maximum relevance and impact.</p>
            </div>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-10 h-10 bg-orange-100 rounded-lg flex items-center justify-center flex-shrink-0">
              <span class="text-lg font-bold text-orange-600">4</span>
            </div>
            <div>
              <h3 class="text-lg font-semibold mb-2">Ongoing Support</h3>
              <p class="text-gray-600 text-sm leading-relaxed">Post-training resources, office hours, and community access ensure continued learning and application after the program ends.</p>
            </div>
          </div>
        </div>
      </div>

      <div class="relative">
        <div class="aspect-[4/3] rounded-3xl overflow-hidden shadow-2xl">
          <img src="/generated/image-business-professionals-collaborating-on--1770142837271-1.webp" alt="Hands-on AI Training" class="w-full h-full object-cover" />
        </div>
      </div>
    </div>
  </section>

  <!-- Success Stories -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 bg-gradient-to-br from-purple-50 to-pink-50 rounded-3xl">
    <div class="text-center max-w-3xl mx-auto mb-16">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Training success stories</h2>
      <p class="text-xl text-gray-600">
        See how organizations are transforming their AI capabilities through our training programs.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
      <!-- Success Story 1 -->
      <div class="bg-white rounded-2xl p-8 shadow-sm border border-gray-200">
        <div class="flex items-center gap-3 mb-6">
          <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center">
            <Briefcase size={24} class="text-blue-600" />
          </div>
          <div>
            <div class="font-semibold text-gray-900">Financial Services Firm</div>
            <div class="text-sm text-gray-500">250 employees trained</div>
          </div>
        </div>
        <p class="text-gray-700 leading-relaxed mb-6 italic">
          "The training program gave our leadership team the confidence to move forward with AI initiatives. Within 3 months of completing the program, we launched our first AI-powered product feature."
        </p>
        <div class="grid grid-cols-3 gap-4 pt-6 border-t border-gray-100">
          <div>
            <div class="text-2xl font-bold text-gray-900">3x</div>
            <div class="text-xs text-gray-600">Faster implementation</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">85%</div>
            <div class="text-xs text-gray-600">Team confidence</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">$1.2M</div>
            <div class="text-xs text-gray-600">Cost savings</div>
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
            <div class="font-semibold text-gray-900">SaaS Technology Company</div>
            <div class="text-sm text-gray-500">120 employees trained</div>
          </div>
        </div>
        <p class="text-gray-700 leading-relaxed mb-6 italic">
          "Our engineering team went from AI novices to confidently building and deploying AI features. The hands-on approach and custom scenarios made all the difference."
        </p>
        <div class="grid grid-cols-3 gap-4 pt-6 border-t border-gray-100">
          <div>
            <div class="text-2xl font-bold text-gray-900">5</div>
            <div class="text-xs text-gray-600">AI features launched</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">92%</div>
            <div class="text-xs text-gray-600">Satisfaction rate</div>
          </div>
          <div>
            <div class="text-2xl font-bold text-gray-900">40%</div>
            <div class="text-xs text-gray-600">Productivity gain</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Training Impact Image -->
    <div class="rounded-2xl overflow-hidden shadow-xl">
      <img src="/generated/image-diverse-corporate-team-having-breakthrou-1770142842368-3.webp" alt="Training Success" class="w-full h-auto object-cover" />
    </div>
  </section>

  <!-- Custom Training Options -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="bg-gradient-to-br from-blue-600 to-purple-600 rounded-3xl p-12 md:p-16 text-white">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Need a custom training program?</h2>
          <p class="text-xl text-blue-100 leading-relaxed mb-8">
            We design bespoke training programs tailored to your organization's specific needs, industry context, and business objectives.
          </p>
          <ul class="space-y-4 mb-8">
            <li class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-200 mt-0.5 flex-shrink-0" />
              <span class="text-blue-50">Custom curriculum aligned with your business goals</span>
            </li>
            <li class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-200 mt-0.5 flex-shrink-0" />
              <span class="text-blue-50">Industry-specific case studies and examples</span>
            </li>
            <li class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-200 mt-0.5 flex-shrink-0" />
              <span class="text-blue-50">Flexible scheduling and delivery formats</span>
            </li>
            <li class="flex items-start gap-3">
              <CheckCircle2 size={20} class="text-blue-200 mt-0.5 flex-shrink-0" />
              <span class="text-blue-50">Ongoing support and follow-up sessions</span>
            </li>
          </ul>
          <a href="#contact" class="inline-flex items-center justify-center gap-2 bg-white text-blue-600 text-base font-medium px-8 py-4 rounded-full hover:bg-blue-50 transition-colors">
            Discuss custom training
            <ArrowRight size={18} />
          </a>
        </div>
        <div class="relative">
          <div class="aspect-[3/4] rounded-2xl overflow-hidden shadow-2xl">
            <img src="/generated/image-confident-female-business-trainer-presen-1770142839445-2.webp" alt="Custom Training" class="w-full h-full object-cover" />
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
                Our programs are designed for various roles including C-suite executives, operations leaders, product managers, engineers, data scientists, and business analysts. We tailor content to each audience's needs and technical level.
              {:else if i === 1}
                Program duration varies by level and format. Executive programs typically run 2-3 days, practitioner programs 5-7 days, and technical programs 10-15 days. We also offer modular formats that can be spread over several weeks.
              {:else if i === 2}
                Yes. We specialize in creating custom training programs tailored to specific industries including financial services, healthcare, retail, manufacturing, and technology. Industry-specific examples and use cases are incorporated throughout.
              {:else if i === 3}
                Our programs are designed for all skill levels. Executive programs require no technical background. Practitioner programs assume basic business technology familiarity. Technical programs require programming experience and data science fundamentals.
              {:else if i === 4}
                Absolutely. We offer virtual instructor-led training with the same interactive, hands-on approach as our in-person programs. Many clients choose hybrid models combining virtual sessions with periodic in-person workshops.
              {:else if i === 5}
                Yes. Participants who complete our training programs receive certificates of completion. Technical programs also offer the option to pursue industry-recognized certifications through our partner organizations.
              {:else if i === 6}
                We use pre and post-training assessments, hands-on project evaluations, and follow-up surveys to measure knowledge gain and application. We also track business outcomes like implementation speed and project success rates.
              {:else if i === 7}
                All programs include post-training resources such as recorded sessions, documentation, and community access. We also offer optional ongoing support packages including office hours, mentoring, and advanced workshops.
              {/if}
            </div>
          {/if}
        </div>
      {/each}
    </div>
  </section>

  <!-- CTA Section -->
  <section id="contact" class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="bg-gradient-to-br from-gray-900 to-gray-800 rounded-3xl p-12 md:p-16 text-center text-white">
      <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-6">Ready to transform your team's AI capabilities?</h2>
      <p class="text-xl text-gray-300 mb-10 max-w-2xl mx-auto">
        Schedule a consultation to discuss your training needs and discover how we can help your organization build world-class AI expertise.
      </p>
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
        <a href="#consultation" class="inline-flex items-center justify-center gap-2 bg-white text-gray-900 text-base font-medium px-8 py-4 rounded-full hover:bg-gray-100 transition-colors">
          Schedule consultation
          <ArrowRight size={18} />
        </a>
        <a href="#programs" class="inline-flex items-center justify-center gap-2 bg-transparent text-white border-2 border-white text-base font-medium px-8 py-4 rounded-full hover:bg-white/10 transition-colors">
          View all programs
        </a>
      </div>
      <p class="text-sm text-gray-400 mt-6">Free needs assessment • Custom program design • Flexible scheduling</p>
    </div>
  </section>
</main>
