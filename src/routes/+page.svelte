<script lang="ts">
  // Icons
  import { Play, Mic, Music, Wand2, Type, Languages, Video, Share2, ArrowRight, Plus, X, Search, Settings, ChevronRight, ChevronDown } from 'lucide-svelte';

  // State for FAQ
  let openFaq = -1;
  const faqs = [
    "What is Studio designed for?",
    "Does Studio support multilingual audio and captions?",
    "Can I assign particular speakers to specific text fragments?",
    "Which file types can I upload?",
    "How does Studio integrate with other tools from your ecosystem?",
    "How do I edit video online with Studio?",
    "Can I add voiceover to video?",
    "How do I add music to video or audio?",
    "Can Studio transcribe audio to text or video to text?",
    "How do I remove background noise from audio or video?",
    "Can I merge videos or fix out-of-sync media?",
    "Does Studio include an online audio editor?"
  ];

  function toggleFaq(index: number) {
    openFaq = openFaq === index ? -1 : index;
  }
</script>

<main class="w-full overflow-hidden">
  <!-- Hero Section -->
  <section class="max-w-[1400px] mx-auto px-6 pt-16 pb-24">
    <div class="flex flex-col lg:flex-row justify-between items-start gap-12 mb-12">
      <div class="max-w-3xl">
        <h1 class="text-5xl md:text-[80px] leading-[0.95] font-medium tracking-tighter mb-10 text-gray-900">
          The best AI audio models<br>in one powerful editor
        </h1>
        <button class="bg-black text-white px-8 py-4 rounded-full font-medium hover:bg-gray-800 transition-colors text-sm">
          Try Studio for free
        </button>
      </div>
      
      <div class="max-w-sm pt-2 lg:pt-4">
        <p class="text-gray-500 text-sm leading-relaxed">
          Built for video creators, podcasters and audiobook authors — bring your stories to life with expressive AI voiceovers, music and sound effects, and real-world recordings.
        </p>
      </div>
    </div>

    <!-- Interface Mockup -->
    <div class="relative w-full aspect-[16/9] bg-[#F3F4F6] rounded-3xl overflow-hidden shadow-2xl border border-gray-200 mt-8">
        <!-- Mockup Content Recreated with CSS -->
        <div class="absolute inset-0 bg-white flex flex-col">
            <!-- Toolbar -->
            <div class="h-14 border-b border-gray-100 flex items-center justify-between px-4 bg-white z-10">
                <div class="flex items-center gap-4">
                    <div class="w-8 h-8 rounded-full bg-gray-100"></div>
                    <div class="text-sm font-medium text-gray-500">ElevenLabs Audio Project</div>
                </div>
                <div class="flex items-center gap-3">
                    <div class="px-3 py-1.5 bg-black text-white text-xs rounded-full">Share</div>
                    <div class="px-3 py-1.5 bg-gray-100 text-black text-xs rounded-full">Export</div>
                </div>
            </div>
            
            <div class="flex-1 flex overflow-hidden">
                <!-- Sidebar -->
                <div class="w-64 border-r border-gray-100 bg-gray-50 p-4 flex flex-col gap-4">
                    <div class="h-24 bg-white rounded-xl border border-gray-100 p-3 shadow-sm">
                        <div class="w-full h-2 bg-gray-100 rounded-full mb-2"></div>
                        <div class="w-2/3 h-2 bg-gray-100 rounded-full"></div>
                    </div>
                     <div class="h-24 bg-white rounded-xl border border-gray-100 p-3 shadow-sm opacity-50"></div>
                     <div class="h-24 bg-white rounded-xl border border-gray-100 p-3 shadow-sm opacity-50"></div>
                </div>
                
                <!-- Main Canvas -->
                <div class="flex-1 bg-white relative flex items-center justify-center">
                    <!-- Gradient Blob -->
                    <div class="absolute w-64 h-64 bg-gradient-to-tr from-orange-400 to-purple-500 rounded-full blur-3xl opacity-20"></div>
                    
                    <!-- Video/Audio Preview -->
                    <div class="relative z-10 w-[60%] aspect-video bg-black rounded-lg overflow-hidden shadow-lg group">
                        <img src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?q=80&w=2070&auto=format&fit=crop" alt="Preview" class="w-full h-full object-cover opacity-80" />
                        <div class="absolute inset-0 flex items-center justify-center">
                             <div class="w-16 h-16 bg-white/20 backdrop-blur-sm rounded-full flex items-center justify-center">
                                <Play class="w-6 h-6 text-white fill-white" />
                             </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Timeline -->
            <div class="h-48 border-t border-gray-100 bg-white p-4 relative">
                <div class="flex items-center justify-between mb-2 text-xs text-gray-400">
                    <span>00:00</span>
                    <span>00:15</span>
                    <span>00:30</span>
                    <span>00:45</span>
                </div>
                <!-- Tracks -->
                <div class="space-y-2">
                    <div class="h-12 bg-blue-50 rounded-lg border border-blue-100 relative overflow-hidden">
                        <div class="absolute inset-y-0 left-0 w-full flex items-center px-2">
                             <!-- Waveform simulation -->
                             <div class="flex items-end gap-[2px] h-6 w-full opacity-50">
                                 {#each Array(100) as _, i}
                                    <div class="w-1 bg-blue-400 rounded-full" style="height: {Math.random() * 100}%"></div>
                                 {/each}
                             </div>
                        </div>
                    </div>
                    <div class="h-12 bg-orange-50 rounded-lg border border-orange-100 relative overflow-hidden w-[80%] ml-[10%]">
                         <div class="absolute inset-y-0 left-0 w-full flex items-center px-2">
                             <!-- Waveform simulation -->
                             <div class="flex items-end gap-[2px] h-6 w-full opacity-50">
                                 {#each Array(80) as _, i}
                                    <div class="w-1 bg-orange-400 rounded-full" style="height: {Math.random() * 100}%"></div>
                                 {/each}
                             </div>
                        </div>
                    </div>
                </div>
                <!-- Playhead -->
                <div class="absolute top-0 bottom-0 left-1/3 w-[1px] bg-red-500 z-20">
                    <div class="absolute top-0 -translate-x-1/2 text-red-500">▼</div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="flex justify-center gap-8 mt-6 text-sm text-gray-400">
        <span class="flex items-center gap-2"><Video size={14} /> Video</span>
        <span class="flex items-center gap-2"><Music size={14} /> Audio</span>
    </div>
  </section>

  <!-- Intro Section -->
  <section class="max-w-[1000px] mx-auto px-6 py-24 text-center">
    <span class="text-sm font-medium text-gray-500 mb-4 block">Introducing Studio 3.0</span>
    <h2 class="text-4xl md:text-5xl font-medium tracking-tight mb-8 leading-tight">
      Create immersive experiences with Studio 3.0 — from podcasts and audiobooks to videos. Enhance your content with AI voices, music, and captions, all in one editor.
    </h2>
    
    <div class="flex flex-wrap justify-center gap-x-6 gap-y-3 text-sm text-gray-600 mb-10">
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Type size={14} /> Text to Speech</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Music size={14} /> Eleven Music</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Wand2 size={14} /> AI Sound Effects</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Type size={14} /> Captions</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Mic size={14} /> Voice Changer</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Type size={14} /> Transcription</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Mic size={14} /> Voice Isolator</span>
      <span class="flex items-center gap-2 px-3 py-1 bg-gray-50 rounded-full border border-gray-100"><Video size={14} /> Video support</span>
    </div>

    <button class="inline-flex items-center gap-2 bg-black text-white pl-3 pr-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
      <div class="w-6 h-6 bg-white rounded-full flex items-center justify-center">
        <Play size={10} class="fill-black text-black ml-0.5" />
      </div>
      Watch intro
    </button>
  </section>

  <!-- Features List Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-12 relative">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-24">
        
        <!-- Feature 1 -->
        <div class="flex flex-col justify-center order-1 md:order-1">
            <h3 class="text-3xl font-medium mb-4">Add new voiceovers</h3>
            <p class="text-gray-600 leading-relaxed mb-6">
                Bring your script to life with natural-sounding voiceovers. Choose from over 10,000 voices - realistic accents, character voices, or professional narration - then edit recordings by simply editing the text.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 order-2 md:order-2">
            <div class="text-xs text-gray-400 mb-4 font-medium uppercase tracking-wide">Select a voice</div>
            <div class="space-y-3">
                {#each [
                    {name: "Burt Reynolds", desc: "Elevated Iconic Voice", img: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=100&auto=format&fit=crop"},
                    {name: "Enrique Montragon", desc: "Middle aged male with a Mexican Spanish accent", img: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?q=80&w=100&auto=format&fit=crop"},
                    {name: "Fin", desc: "A well-connected, young conversational male", img: "https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?q=80&w=100&auto=format&fit=crop"},
                    {name: "Hope", desc: "A warm, soothing, and captivating voice", img: "https://images.unsplash.com/photo-1494790108377-be9c29b29330?q=80&w=100&auto=format&fit=crop"},
                    {name: "Magic Jack", desc: "Casual, friendly, heart-felt voice", img: "https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?q=80&w=100&auto=format&fit=crop"},
                    {name: "Jack Bass", desc: "A calm and gritty storyteller", img: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?q=80&w=100&auto=format&fit=crop"},
                ] as voice}
                <div class="flex items-center gap-3 p-2 hover:bg-white rounded-lg transition-colors cursor-pointer group">
                    <img src={voice.img} alt={voice.name} class="w-10 h-10 rounded-full object-cover" />
                    <div>
                        <div class="text-sm font-medium text-gray-900">{voice.name}</div>
                        <div class="text-xs text-gray-500">{voice.desc}</div>
                    </div>
                    <div class="ml-auto opacity-0 group-hover:opacity-100">
                        <div class="w-8 h-8 rounded-full border border-gray-200 flex items-center justify-center bg-white">
                            <Play size={12} class="fill-black text-black ml-0.5" />
                        </div>
                    </div>
                </div>
                {/each}
            </div>
        </div>

        <!-- Feature 2 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[400px] flex items-center justify-center order-4 md:order-3 relative overflow-hidden">
             <!-- Abstract visualization for music -->
             <div class="absolute inset-0 flex items-center justify-center">
                 <div class="w-full h-full bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-orange-100 via-gray-50 to-gray-50"></div>
                 <div class="absolute w-64 h-64 border border-orange-200 rounded-full flex items-center justify-center animate-pulse">
                     <div class="w-48 h-48 border border-orange-300 rounded-full flex items-center justify-center">
                         <div class="w-32 h-32 bg-orange-500/10 rounded-full backdrop-blur-sm"></div>
                     </div>
                 </div>
             </div>
        </div>
        <div class="flex flex-col justify-center order-3 md:order-4">
            <h3 class="text-3xl font-medium mb-4">Generate bespoke background music with Eleven Music</h3>
            <p class="text-gray-600 leading-relaxed">
                Create music that feels custom-made for your content. Generate soundtracks in any genre or style, or let Studio auto-score your video with music created to match your scene.
            </p>
        </div>

        <!-- Feature 3 -->
        <div class="flex flex-col justify-center order-5 md:order-5">
            <h3 class="text-3xl font-medium mb-4">Add custom sound effects</h3>
            <p class="text-gray-600 leading-relaxed">
                Enrich your content with any sound effect you can describe with a prompt. From subtle ambience to cinematic impact, add effects directly in Studio for a polished production.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-6 md:order-6">
             <div class="w-full max-w-xs bg-white rounded-xl shadow-sm p-4 border border-gray-100">
                 <div class="flex items-center gap-3 mb-3">
                     <div class="w-8 h-8 bg-purple-100 rounded-lg flex items-center justify-center text-purple-600">
                         <Wand2 size={16} />
                     </div>
                     <div class="text-sm font-medium">Sound Effect Generator</div>
                 </div>
                 <div class="h-2 bg-gray-100 rounded-full mb-2 w-full"></div>
                 <div class="h-2 bg-gray-100 rounded-full w-2/3"></div>
             </div>
        </div>

        <!-- Feature 4 -->
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-8 md:order-7">
            <div class="relative w-full max-w-md bg-white rounded-xl shadow-sm p-6 border border-gray-100">
                <div class="text-lg font-medium mb-2">"I think we should go to the <span class="bg-red-100 text-red-800 px-1 rounded line-through decoration-red-500">beach</span> <span class="bg-green-100 text-green-800 px-1 rounded">mountains</span> tomorrow."</div>
                <div class="flex items-center gap-2 mt-4 text-xs text-gray-500">
                    <span class="px-2 py-1 bg-gray-100 rounded">Original</span>
                    <ArrowRight size={12} />
                    <span class="px-2 py-1 bg-green-50 text-green-700 border border-green-100 rounded">Corrected</span>
                </div>
            </div>
        </div>
        <div class="flex flex-col justify-center order-7 md:order-8">
            <h3 class="text-3xl font-medium mb-4">Fix mistakes in seconds with Speech Correction</h3>
            <p class="text-gray-600 leading-relaxed">
                Edit spoken audio instantly using AI voice cloning. Just change the script, and Studio regenerates the same voice — no re-recording, no extra takes.
            </p>
        </div>

        <!-- Feature 5 -->
        <div class="flex flex-col justify-center order-9 md:order-9">
            <h3 class="text-3xl font-medium mb-4">Clean up noisy audio with Voice Isolator</h3>
            <p class="text-gray-600 leading-relaxed">
                Remove background noise, reverb, and distractions with AI-powered noise reduction. Enhance audio quality so every word is crystal clear.
            </p>
        </div>
        <div class="bg-gray-50 rounded-2xl p-6 border border-gray-100 min-h-[300px] flex items-center justify-center order-10 md:order-10">
             <div class="w-full max-w-sm space-y-4">
                 <div class="bg-white p-4 rounded-xl border border-gray-100 shadow-sm">
                     <div class="flex justify-between text-xs text-gray-500 mb-2">
                         <span>Noisy Input</span>
                         <Mic size={14} />
                     </div>
                     <div class="flex items-center gap-1 h-8 opacity-40">
                         {#each Array(20) as _, i}
                            <div class="flex-1 bg-gray-800 rounded-full" style="height: {30 + Math.random() * 70}%"></div>
                         {/each}
                     </div>
                 </div>
                 <div class="flex justify-center">
                     <div class="bg-black text-white p-2 rounded-full">
                         <ArrowRight size={16} class="rotate-90" />
                     </div>
                 </div>
                 <div class="bg-white p-4 rounded-xl border border-green-100 shadow-sm ring-1 ring-green-50">
                     <div class="flex justify-between text-xs text-green-600 mb-2">
                         <span>Clean Output</span>
                         <span class="font-bold">100% Clear</span>
                     </div>
                     <div class="flex items-center gap-1 h-8">
                         {#each Array(20) as _, i}
                            <div class="flex-1 bg-green-500 rounded-full" style="height: {20 + Math.random() * 60}%"></div>
                         {/each}
                     </div>
                 </div>
             </div>
        </div>
    </div>
  </section>
  
  <!-- Floating Action Bar (Stickyish) -->
  <div class="sticky bottom-6 z-40 flex justify-center pointer-events-none">
      <div class="bg-white/80 backdrop-blur-md border border-gray-200 shadow-lg rounded-full py-3 px-6 flex items-center gap-6 pointer-events-auto">
          <span class="text-sm font-medium text-gray-900 hidden sm:block">The best AI audio models in one powerful editor</span>
          <button class="bg-black text-white text-xs font-bold px-4 py-2 rounded-full hover:bg-gray-800 transition-colors">
              Sign up
          </button>
      </div>
  </div>

  <!-- Seamless Timeline Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
    <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">All your creative tools, in one seamless timeline</h2>
        <p class="text-gray-600">From captions and collaboration to video editing and multilingual audio, Studio 3.0 combines every tool you need to edit, produce, and share at scale.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <!-- Card 1: Timeline (Wide) -->
        <div class="md:col-span-2 bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10 max-w-md">
                <h3 class="text-xl font-medium mb-2">Timeline</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Trim, merge, and edit audio and video with precision. Sync voiceovers, music, and sound effects on a single intuitive editing timeline.</p>
            </div>
            <div class="absolute right-0 bottom-0 w-2/3 h-2/3 translate-x-10 translate-y-10">
                 <!-- Timeline abstract visual -->
                 <div class="w-full h-full bg-white rounded-tl-xl shadow-lg border border-gray-100 p-4 transform -rotate-6">
                     <div class="space-y-2">
                         <div class="h-8 bg-blue-100 rounded w-full"></div>
                         <div class="h-8 bg-orange-100 rounded w-3/4 ml-12"></div>
                         <div class="h-8 bg-purple-100 rounded w-1/2 ml-24"></div>
                     </div>
                 </div>
            </div>
        </div>

        <!-- Card 2: Video Support -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
             <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Video support</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Upload MP4 or MOV files and enhance them with AI. Add voiceovers, background music, sound effects, and auto captions.</p>
            </div>
            <div class="absolute inset-x-0 bottom-0 h-40 bg-gradient-to-t from-gray-200 to-transparent"></div>
            <div class="absolute bottom-4 right-4 left-4 h-32 bg-black rounded-lg shadow-lg overflow-hidden">
                <img src="https://images.unsplash.com/photo-1626814026160-2237a95fc5a0?q=80&w=2070&auto=format&fit=crop" class="w-full h-full object-cover opacity-80" alt="Video" />
                <div class="absolute inset-0 flex items-center justify-center">
                    <Play class="text-white fill-white w-8 h-8" />
                </div>
            </div>
        </div>

        <!-- Card 3: Captions -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Captions</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Generate captions in one click for accessibility and engagement. Customize style, add multilingual subtitles.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 flex gap-4">
                <div class="flex-1 bg-black text-white p-3 rounded-lg text-xs text-center shadow-lg">
                    Minimal Clean
                </div>
                <div class="flex-1 bg-white text-black border border-gray-200 p-3 rounded-lg text-xs text-center shadow-sm">
                    Trendy Outline
                </div>
            </div>
        </div>

        <!-- Card 4: Public Project URLs -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">Public project URLs</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Share editable links for client or team feedback. Collect time-stamped comments directly on the timeline.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 bg-white rounded-xl border border-gray-100 p-3 shadow-md">
                <div class="flex items-center gap-3 mb-2">
                    <div class="w-8 h-8 bg-blue-500 rounded-full flex items-center justify-center text-white text-xs">KC</div>
                    <div>
                        <div class="text-xs font-bold">Kevin Cander</div>
                        <div class="text-[10px] text-gray-500">Good catch! Fixed.</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Card 5: Language Support -->
        <div class="bg-gray-50 rounded-3xl p-8 border border-gray-100 overflow-hidden relative min-h-[300px]">
            <div class="relative z-10">
                <h3 class="text-xl font-medium mb-2">32+ Language support</h3>
                <p class="text-sm text-gray-600 leading-relaxed">Produce audio and video in over 32 languages with expressive accents and localized narration tailored to your audience.</p>
            </div>
            <div class="absolute bottom-6 left-6 right-6 space-y-2">
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100">
                    <span class="text-lg">🇪🇸</span> <span class="text-xs font-medium">Spanish</span>
                </div>
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100 ml-4">
                    <span class="text-lg">🇬🇧</span> <span class="text-xs font-medium">English</span>
                </div>
                <div class="bg-white rounded-lg p-2 flex items-center gap-2 shadow-sm border border-gray-100">
                    <span class="text-lg">🇩🇪</span> <span class="text-xs font-medium">German</span>
                </div>
            </div>
        </div>
    </div>
  </section>

  <!-- Built for Every Creator -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Built for every creator</h2>
        <p class="text-gray-600">From video creators to podcasters and audiobook authors, Studio 3.0 adapts to every workflow — combining AI audio editing, video editing, and professional sound design.</p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Creator 1 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="https://images.unsplash.com/photo-1478737270239-2f02b77ac6d5?q=80&w=2070&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Audiobook" />
                <div class="absolute inset-0 bg-gradient-to-t from-blue-900/60 to-transparent mix-blend-multiply"></div>
                <!-- Color overlay effect similar to screenshot -->
                <div class="absolute inset-0 bg-blue-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Audiobook authors</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Revive narration instantly with text-based editing, enrich audio with custom soundscapes, and generate cinematic audiobook trailers.</p>
        </div>

        <!-- Creator 2 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="https://images.unsplash.com/photo-1590602847861-f357a9332bbc?q=80&w=2070&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Podcaster" />
                <div class="absolute inset-0 bg-gradient-to-t from-orange-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-orange-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">Podcasters</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Clean up dialogue with noise removal, fix mistakes without re-recording, and design custom theme music or soundscapes for every episode.</p>
        </div>

        <!-- Creator 3 -->
        <div class="group">
            <div class="aspect-square rounded-2xl overflow-hidden mb-6 relative">
                <img src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?q=80&w=2080&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105" alt="Filmmaker" />
                <div class="absolute inset-0 bg-gradient-to-t from-red-900/60 to-transparent mix-blend-multiply"></div>
                <div class="absolute inset-0 bg-red-500/20 mix-blend-color"></div>
            </div>
            <h3 class="text-lg font-medium mb-2">AI filmmakers</h3>
            <p class="text-xs text-gray-500 leading-relaxed">Combine video, audio, and AI-generated music to prototype scenes, add voiceovers, and experiment with sound design inside a single editor.</p>
        </div>
    </div>
  </section>

  <!-- API Section -->
  <section class="max-w-[1400px] mx-auto px-6 py-24">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-4xl font-medium tracking-tight mb-4">Everything in Studio, available through our API</h2>
        <p class="text-gray-600">Access the same voices, music, and audio tools behind Studio 3.0 — programmatically, at scale, in any workflow.</p>
    </div>

    <div class="max-w-3xl mx-auto bg-white rounded-xl border border-gray-200 shadow-sm p-6 md:p-10 font-mono text-xs md:text-sm overflow-x-auto">
        <div class="text-gray-800">
            <span class="text-purple-600">import</span> {`{ ElevenLabsClient }`} <span class="text-purple-600">from</span> <span class="text-green-600">"elevenlabs-client"</span>;<br><br>
            <span class="text-purple-600">const</span> client = <span class="text-purple-600">new</span> <span class="text-yellow-600">ElevenLabsClient</span>({`{ apiKey: "YOUR_API_KEY" }`});<br>
            <span class="text-purple-600">await</span> client.textToSpeech.<span class="text-blue-600">convert</span>("JBFqnCBsd6J8dqVD02eK", {`{`}<br>
            &nbsp;&nbsp;output_format: <span class="text-green-600">"mp3_44100_128"</span>,<br>
            &nbsp;&nbsp;text: <span class="text-green-600">"The first move is what sets everything in motion."</span>,<br>
            &nbsp;&nbsp;model_id: <span class="text-green-600">"eleven_multilingual_v2"</span>,<br>
            `});`
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
                    <span class="text-sm md:text-base text-gray-700 group-hover:text-black transition-colors">{question}</span>
                    <span class="text-gray-400">
                        <Plus size={16} class="transition-transform duration-200 {openFaq === i ? 'rotate-45' : ''}" />
                    </span>
                </button>
                {#if openFaq === i}
                    <div class="mt-4 text-sm text-gray-500 leading-relaxed pb-2">
                        Studio is designed for creators who want to produce high-quality audio and video content efficiently. It combines advanced AI tools for voice generation, music creation, and sound effects with a timeline-based editor.
                    </div>
                {/if}
            </div>
          {/each}
      </div>
  </section>

  <!-- Bottom CTA -->
  <section class="max-w-[1400px] mx-auto px-6 py-24 flex flex-col items-center text-center border-t border-gray-100">
      <h2 class="text-4xl font-medium tracking-tight mb-8">The most realistic voice AI platform</h2>
      <div class="flex items-center gap-4">
          <button class="bg-black text-white px-6 py-3 rounded-full font-medium hover:bg-gray-800 transition-colors text-sm">
              Create an AI agent
          </button>
          <button class="bg-white text-black border border-gray-200 px-6 py-3 rounded-full font-medium hover:bg-gray-50 transition-colors text-sm">
              Talk to sales
          </button>
      </div>
  </section>
</main>

<style>
    /* Custom scrollbar hide for clean look in some areas if needed */
    .no-scrollbar::-webkit-scrollbar {
        display: none;
    }
    .no-scrollbar {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>

