<script lang="ts">
  import { ArrowRight, Mail, Phone, MapPin, Clock, Send, CheckCircle2, MessageSquare, Calendar, Users } from 'lucide-svelte';

  // Form state
  let formData = $state({
    name: '',
    email: '',
    company: '',
    phone: '',
    service: '',
    message: '',
    budget: '',
    timeline: ''
  });

  let formSubmitted = $state(false);
  let isSubmitting = $state(false);

  // Office locations
  const offices = [
    {
      city: "San Francisco",
      address: "123 Market Street, Suite 400",
      region: "San Francisco, CA 94103",
      timezone: "PST"
    },
    {
      city: "New York",
      address: "456 Broadway, Floor 12",
      region: "New York, NY 10013",
      timezone: "EST"
    },
    {
      city: "Austin",
      address: "789 Congress Ave, Suite 200",
      region: "Austin, TX 78701",
      timezone: "CST"
    }
  ];

  // Service options
  const services = [
    "AI Workflow Integration",
    "Internal Tool Development",
    "GTM Product Development",
    "Strategic AI Planning",
    "Rapid Pilot Program",
    "Other"
  ];

  function handleSubmit(e: Event) {
    e.preventDefault();
    isSubmitting = true;
    
    // Simulate form submission
    setTimeout(() => {
      formSubmitted = true;
      isSubmitting = false;
    }, 1500);
  }
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section -->
  <section class="pt-16 md:pt-24 pb-12">
    <div class="max-w-[1400px] mx-auto px-6 md:px-10">
      
      <!-- Breadcrumb -->
      <div class="flex items-center gap-2 text-sm text-gray-500 mb-8">
        <a href="/" class="hover:text-gray-900 transition-colors">Home</a>
        <ArrowRight size={14} />
        <span class="text-gray-900 font-medium">Contact</span>
      </div>

      <!-- Hero Content -->
      <div class="max-w-3xl mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 bg-blue-50 rounded-full text-sm font-medium text-blue-700 mb-6">
          <MessageSquare size={16} />
          Get in touch
        </div>
        <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black mb-6 leading-[1.1]">
          Let's transform your business together
        </h1>
        <p class="text-xl text-gray-600 leading-relaxed">
          Ready to accelerate your AI transformation? Our team of experts is here to help you implement solutions that deliver measurable results. Schedule a free consultation to discuss your needs.
        </p>
      </div>

    </div>
  </section>

  <!-- Contact Form Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-12">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
      
      <!-- Form -->
      <div>
        <h2 class="text-3xl font-medium mb-4">Send us a message</h2>
        <p class="text-gray-600 mb-8">
          Fill out the form below and our team will get back to you within 24 hours. For urgent inquiries, please call us directly.
        </p>

        {#if !formSubmitted}
          <form onsubmit={handleSubmit} class="space-y-6">
            <!-- Name & Email -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label for="name" class="block text-sm font-medium text-gray-700 mb-2">
                  Full name *
                </label>
                <input
                  type="text"
                  id="name"
                  bind:value={formData.name}
                  required
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all"
                  placeholder="John Smith"
                />
              </div>
              <div>
                <label for="email" class="block text-sm font-medium text-gray-700 mb-2">
                  Email address *
                </label>
                <input
                  type="email"
                  id="email"
                  bind:value={formData.email}
                  required
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all"
                  placeholder="john@company.com"
                />
              </div>
            </div>

            <!-- Company & Phone -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label for="company" class="block text-sm font-medium text-gray-700 mb-2">
                  Company name
                </label>
                <input
                  type="text"
                  id="company"
                  bind:value={formData.company}
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all"
                  placeholder="Acme Inc."
                />
              </div>
              <div>
                <label for="phone" class="block text-sm font-medium text-gray-700 mb-2">
                  Phone number
                </label>
                <input
                  type="tel"
                  id="phone"
                  bind:value={formData.phone}
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all"
                  placeholder="+1 (555) 123-4567"
                />
              </div>
            </div>

            <!-- Service & Budget -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label for="service" class="block text-sm font-medium text-gray-700 mb-2">
                  Service interested in *
                </label>
                <select
                  id="service"
                  bind:value={formData.service}
                  required
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all bg-white"
                >
                  <option value="">Select a service</option>
                  {#each services as service}
                    <option value={service}>{service}</option>
                  {/each}
                </select>
              </div>
              <div>
                <label for="budget" class="block text-sm font-medium text-gray-700 mb-2">
                  Budget range
                </label>
                <select
                  id="budget"
                  bind:value={formData.budget}
                  class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all bg-white"
                >
                  <option value="">Select budget range</option>
                  <option value="under-50k">Under $50k</option>
                  <option value="50k-100k">$50k - $100k</option>
                  <option value="100k-250k">$100k - $250k</option>
                  <option value="250k-plus">$250k+</option>
                </select>
              </div>
            </div>

            <!-- Timeline -->
            <div>
              <label for="timeline" class="block text-sm font-medium text-gray-700 mb-2">
                Project timeline
              </label>
              <select
                id="timeline"
                bind:value={formData.timeline}
                class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all bg-white"
              >
                <option value="">Select timeline</option>
                <option value="immediate">Immediate (within 2 weeks)</option>
                <option value="1-month">Within 1 month</option>
                <option value="1-3-months">1-3 months</option>
                <option value="3-plus-months">3+ months</option>
                <option value="exploring">Just exploring</option>
              </select>
            </div>

            <!-- Message -->
            <div>
              <label for="message" class="block text-sm font-medium text-gray-700 mb-2">
                Tell us about your project *
              </label>
              <textarea
                id="message"
                bind:value={formData.message}
                required
                rows="5"
                class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 outline-none transition-all resize-none"
                placeholder="Describe your business challenges, goals, and what you're hoping to achieve with AI implementation..."
              ></textarea>
            </div>

            <!-- Submit Button -->
            <button
              type="submit"
              disabled={isSubmitting}
              class={[
                'w-full inline-flex items-center justify-center gap-2 bg-black text-white text-base font-medium px-8 py-4 rounded-full transition-all',
                isSubmitting ? 'opacity-50 cursor-not-allowed' : 'hover:bg-gray-800'
              ]}
            >
              {#if isSubmitting}
                Sending...
              {:else}
                Send message
                <Send size={18} />
              {/if}
            </button>

            <p class="text-xs text-gray-500 text-center">
              By submitting this form, you agree to our privacy policy and terms of service.
            </p>
          </form>
        {:else}
          <!-- Success Message -->
          <div class="bg-green-50 rounded-2xl p-8 border border-green-200 text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <CheckCircle2 size={32} class="text-green-600" />
            </div>
            <h3 class="text-2xl font-semibold mb-3">Message sent successfully!</h3>
            <p class="text-gray-600 mb-6">
              Thank you for reaching out. Our team will review your message and get back to you within 24 hours.
            </p>
            <button
              onclick={() => formSubmitted = false}
              class="inline-flex items-center gap-2 text-green-600 font-medium hover:text-green-700"
            >
              Send another message
              <ArrowRight size={16} />
            </button>
          </div>
        {/if}
      </div>

      <!-- Sidebar Info -->
      <div class="space-y-8">
        
        <!-- Why Contact Us -->
        <div class="bg-gradient-to-br from-blue-50 to-indigo-50 rounded-2xl p-8 border border-blue-100">
          <h3 class="text-xl font-semibold mb-4">What to expect</h3>
          <ul class="space-y-4">
            <li class="flex items-start gap-3">
              <div class="w-6 h-6 bg-blue-600 rounded-full flex items-center justify-center flex-shrink-0 mt-0.5">
                <CheckCircle2 size={14} class="text-white" />
              </div>
              <div>
                <div class="font-medium text-gray-900 mb-1">Free consultation</div>
                <div class="text-sm text-gray-600">30-minute discovery call to understand your needs</div>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <div class="w-6 h-6 bg-blue-600 rounded-full flex items-center justify-center flex-shrink-0 mt-0.5">
                <CheckCircle2 size={14} class="text-white" />
              </div>
              <div>
                <div class="font-medium text-gray-900 mb-1">Custom proposal</div>
                <div class="text-sm text-gray-600">Tailored implementation roadmap with ROI projections</div>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <div class="w-6 h-6 bg-blue-600 rounded-full flex items-center justify-center flex-shrink-0 mt-0.5">
                <CheckCircle2 size={14} class="text-white" />
              </div>
              <div>
                <div class="font-medium text-gray-900 mb-1">Rapid pilot option</div>
                <div class="text-sm text-gray-600">Start with a 2-4 week pilot to demonstrate value</div>
              </div>
            </li>
            <li class="flex items-start gap-3">
              <div class="w-6 h-6 bg-blue-600 rounded-full flex items-center justify-center flex-shrink-0 mt-0.5">
                <CheckCircle2 size={14} class="text-white" />
              </div>
              <div>
                <div class="font-medium text-gray-900 mb-1">No commitment required</div>
                <div class="text-sm text-gray-600">Explore options with zero obligation</div>
              </div>
            </li>
          </ul>
        </div>

        <!-- Office Hours -->
        <div class="bg-white rounded-2xl p-8 border border-gray-200">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center">
              <Clock size={20} class="text-gray-700" />
            </div>
            <h3 class="text-lg font-semibold">Office hours</h3>
          </div>
          <div class="space-y-2 text-sm">
            <div class="flex justify-between py-2 border-b border-gray-100">
              <span class="text-gray-600">Monday - Friday</span>
              <span class="font-medium text-gray-900">9:00 AM - 6:00 PM EST</span>
            </div>
            <div class="flex justify-between py-2 border-b border-gray-100">
              <span class="text-gray-600">Saturday</span>
              <span class="font-medium text-gray-900">10:00 AM - 2:00 PM EST</span>
            </div>
            <div class="flex justify-between py-2">
              <span class="text-gray-600">Sunday</span>
              <span class="font-medium text-gray-900">Closed</span>
            </div>
          </div>
          <div class="mt-4 p-3 bg-blue-50 rounded-lg text-xs text-gray-700">
            For urgent matters outside business hours, please email us and we'll respond as soon as possible.
          </div>
        </div>
      </div>
    </div>
  </section>
</main>
